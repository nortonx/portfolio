<template>
  <div class="container mx-auto max-w-2xl">
    <main class="p-2">
      <h1>Another Layout</h1>
      <slot />
    </main>
  </div>
</template>

<script lang="ts" setup>
useHead({
  titleTemplate: "%s - Norton Almeida (Another Layout)",
})
</script>
