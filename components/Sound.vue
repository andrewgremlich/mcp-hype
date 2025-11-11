<template>
  <div>
    <button @click="playSound">
      +
    </button>
  </div>
</template>

<script setup lang="ts">
import { watch } from 'vue'
import { useSound } from '@vueuse/sound'
import { useNav } from '@slidev/client'
import buttonSfx from '/slide-whistle-up.mp3?url'

const { play } = useSound(buttonSfx)
const { currentPage } = useNav()

watch(currentPage, () => {
  play()
})

const playSound = () => {
  play()
}
</script>
