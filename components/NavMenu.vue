<template>
  <header class="flex justify-between items-center bg-gray-100 dark:bg-gray-800 p-4">
    <div class="flex items-center space-x-12">
      <div>
        <nuxt-link to="/" class="text-xl font-semibold link">Norton Almeida</nuxt-link>
      </div>
      <nav class="font-mono">
        <ul class="flex space-x-4">
          <li v-for="link in links" :key="link.url">
            <nuxt-link :to="link.url" class="link">{{ link.name }}</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
    <client-only>
      <ColorModeSelector />
    </client-only>
  </header>
</template>

<script lang="ts" setup>

const links = [
  { name: 'Home', url: '/' },
  { name: 'Blog', url: '/blog' },
  { name: 'Projects', url: '/projects' },
  { name: 'About', url: '/about' },
]
</script>

<style scoped>
  .link {
    @apply p-2 hover:bg-gray-200 text-gray-700 dark:text-white hover:dark:bg-gray-700;
  }
</style>