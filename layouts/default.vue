<template>
  <div class="container mx-auto max-w-2xl">
    <NavMenu />
    <main class="p-2 mt-10">
      <slot />
    </main>
  </div>
</template>

<script lang="ts" setup>
const colorMode = useColorMode()

useSeoMeta({
  titleTemplate: "%s - Norton Almeida",
})
</script>

<style>
body {
  @apply bg-white dark:bg-gray-800 text-gray-700 dark:text-white;
}
</style>
