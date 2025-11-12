<template>
  <div class="permanently-show">
    <button 
      @click="toggleMute"
      :aria-label="isMuted ? 'Unmute sounds' : 'Mute sounds'"
      :title="isMuted ? 'Unmute sounds' : 'Mute sounds'"
      type="button"
      role="button"
      tabindex="0"
    >
      <carbon:volume-up v-if="isMuted" size="8" />
      <carbon:volume-mute v-else size="8" />
    </button>
  </div>
</template>

<style scoped>
.permanently-show {
  position: fixed;
  top: 1rem;
  right: 1rem;
  z-index: 1000;
}

.permanently-show button {
  background: transparent;
  border: none;
  padding: 0;
  opacity: 0.6;
  transition: opacity 0.3s;
}

.permanently-show button:hover {
  opacity: 1;
}
</style>

<script setup lang="ts">
import { watch, ref } from 'vue'
import { useSound } from '@vueuse/sound'
import { useNav } from '@slidev/client'

const props = defineProps<{
  soundFiles: string[]
}>()

const { currentPage } = useNav()

const soundInstances = ref<Record<string, any>>({})
const usedSounds = ref<Set<string>>(new Set())
const isMuted = ref(true)

props.soundFiles.forEach(file => {
  const { play } = useSound(file)
  soundInstances.value[file] = play
})

const getRandomSound = () => {
  if (usedSounds.value.size >= props.soundFiles.length) {
    usedSounds.value.clear()
  }
  
  const availableSounds = props.soundFiles.filter(file => !usedSounds.value.has(file))
  
  const randomIndex = Math.floor(Math.random() * availableSounds.length)
  const randomFile = availableSounds[randomIndex]
  
  usedSounds.value.add(randomFile)
  
  return soundInstances.value[randomFile]
}

const playRandomSound = () => {
  if (isMuted.value) return
  
  const randomPlay = getRandomSound()
  randomPlay()
}

const toggleMute = () => {
  isMuted.value = !isMuted.value
}

watch(currentPage, () => {
  playRandomSound()
})
</script>