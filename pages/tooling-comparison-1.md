---
transition: slide-up
---

```ts {monaco}
export async function getForecast(latitude: number, longitude: number): Promise<string> {
  const pointsUrl = `${NWS_API_BASE}/points/${latitude.toFixed(4)},${longitude.toFixed(4)}`;
  const pointsData = await makeNWSRequest<PointsResponse>(pointsUrl);

  if (!pointsData)
    return `Failed to retrieve grid point data for coordinates: ${latitude}, ${longitude}. This location may not be supported by the NWS API.`;

  const forecastUrl = pointsData.properties?.forecast;
  if (!forecastUrl) return "Failed to get forecast URL from grid point data";

  const forecastData = await makeNWSRequest<ForecastResponse>(forecastUrl);
  if (!forecastData) return "Failed to retrieve forecast data";

  const periods = forecastData.properties?.periods || [];
  if (periods.length === 0) return "No forecast periods available";

  const formattedForecast = periods.map((p) =>
    [
      `${p.name || "Unknown"}:`,
      `Temperature: ${p.temperature || "Unknown"}°${p.temperatureUnit || "F"}`,
      `Wind: ${p.windSpeed || "Unknown"} ${p.windDirection || ""}`,
      `${p.shortForecast || "No forecast available"}`,
      "---",
    ].join("\n")
  );

  return `Forecast for ${latitude}, ${longitude}:\n\n${formattedForecast.join("\n")}`;
}
```
