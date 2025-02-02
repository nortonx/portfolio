<template>
  <div>
    <h1>This is the About page</h1>
  </div>
</template>

<script lang="ts" setup>

definePageMeta({
  layout: "another"
})

useHead({
  title: "About"
})
</script>
