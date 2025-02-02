<template>
  <div class="flex space-x-2 items-center">
    <div v-if="showNextModeLabel" class="text-slate-500 text-xs">Change to {{ nextMode }}</div>
    <button 
      @click="toggleMode"
      @mouseenter="showNextModeLabel = true"
      @mouseleave="showNextModeLabel = false"
      class="hover:bg-gray-300 hover:dark:bg-gray-600 px-2 py-1 text-gray-500">{{ nextModeIcon }}</button>
  </div>
</template>

<script lang="ts" setup>
const showNextModeLabel = ref(false)
const colorMode = useColorMode()
const modes = [
  'system',
  'light',
  'dark'
]

const nextModeIcons = {
  system: '🌞🌜',
  light: '🌞',
  dark: '🌜'
}

const nextMode = computed(()=> {
  const currentIndex = modes.indexOf(colorMode.preference)
  let nextModeIndex = (currentIndex + 1) % modes.length
  return modes[nextModeIndex]
})

const nextModeIcon = computed(() => nextModeIcons[nextMode.value])

const toggleMode = () => {
  colorMode.preference = nextMode.value
}
</script>
