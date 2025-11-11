<template>
  <a :href="value" target="_blank" id="prezi-qrcode">
    <qrcode-vue :size="size" :margin="margin" :value="value" :level="level" :render-as="renderAs" :background="background" :foreground='foreground'
      :gradient="gradient" :gradient-type="gradientType" :gradient-start-color="gradientStartColor"
      :gradient-end-color="gradientEndColor" :image-settings='imageSettings' />
  </a>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import QrcodeVue from 'qrcode.vue'
import type { Level, RenderAs, GradientType, ImageSettings } from 'qrcode.vue'

const props = defineProps<{
  urlToEncode: string
}>()

const value = ref(props.urlToEncode)
const level = ref<Level>('M')
const renderAs = ref<RenderAs>('svg')
const background = ref('#ffffff')
const foreground = ref('#000000')
const margin = ref(2)
const size = ref(150)

const imageSettings = ref<ImageSettings>({
  src: 'https://creazilla-store.fra1.digitaloceanspaces.com/silhouettes/840403/wizard-hat-silhouette-000000-md.png',
  width: 30,
  height: 30,
  excavate: true,
})

const gradient = ref(true)
const gradientType = ref<GradientType>('radial')
const gradientStartColor = ref('#000000')
const gradientEndColor = ref('#004f3b')
</script>