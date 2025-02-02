<template>
  <div>
    <h1>This is the nuxt index page</h1>
  </div>
</template>

<script lang="ts" setup>
useSeoMeta({
  title: 'Index',
  description: 'This is the nuxt index page',
  image: 'https://nortonalmeida.dev/norton-almeida.jpg',
  url: 'https://nortonalmeida.dev',
  type: 'website',
  keywords: ['norton', 'almeida', 'norton almeida', 'nortonalmeida', 'norton almeida website'],
})
</script>