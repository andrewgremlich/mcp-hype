<template>
  <div>
    <button @click="playSound">
      +
    </button>
  </div>
</template>

<script setup lang="ts">
import { useSound } from '@vueuse/sound'
import buttonSfx from '/whoosh_0.webm?url'

const { play } = useSound(buttonSfx)

const playSound = () => {
  play()
}
</script>
