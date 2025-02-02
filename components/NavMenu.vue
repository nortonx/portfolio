<template>
  <header class="flex justify-between items-center bg-gray-100 p-4">
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
    @apply p-2 hover:bg-gray-200
  }
</style>