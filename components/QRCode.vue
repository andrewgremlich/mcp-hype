<template>
  <a :href="urlToEncode" target="_blank">
    <qrcode-vue :value="urlToEncode" :size="150" :margin="margin" render-as="svg" />
  </a>
</template>

<script setup lang="ts">
import { ref } from "vue";
import QrcodeVue from "qrcode.vue";

defineProps<{ urlToEncode: string }>();

const margin = ref(2);
</script>
