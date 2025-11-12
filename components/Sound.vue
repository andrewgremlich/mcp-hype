<template>
  <div>
    <button @click="playRandomSound">
      +
    </button>
  </div>
</template>

<script setup lang="ts">
import { watch, ref } from 'vue'
import { useSound } from '@vueuse/sound'
import { useNav } from '@slidev/client'

const props = defineProps<{
  soundFiles: string[]
}>()

const { currentPage } = useNav()

// Create sound instances for all files
const soundInstances = ref<Record<string, any>>({})

// Initialize all sound instances
props.soundFiles.forEach(file => {
  const { play } = useSound(file)
  soundInstances.value[file] = play
})

const getRandomSound = () => {
  const randomIndex = Math.floor(Math.random() * props.soundFiles.length)
  const randomFile = props.soundFiles[randomIndex]
  return soundInstances.value[randomFile]
}

const playRandomSound = () => {
  const randomPlay = getRandomSound()
  randomPlay()
}

watch(currentPage, () => {
  playRandomSound()
})
</script>