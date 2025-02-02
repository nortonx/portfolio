<template>
  <div class="container mx-auto max-w-2xl">
    <NavMenu />
    <main class="p-2">
      <slot />
    </main>
  </div>
</template>

<script lang="ts" setup>
useSeoMeta({
  titleTemplate: "%s - Norton Almeida",
})
</script>
