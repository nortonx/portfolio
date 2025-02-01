<template>
  <div>
    <h1>This is the Blog slug page</h1>
    <p>Route params: {{ route.params }}</p>
  </div>
</template>

<script lang="ts" setup>
const route = useRoute()
</script>