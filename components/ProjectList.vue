<template>
  <div>
    <section v-if="pending">Loading...</section>
    <section v-else-if="error">Error: {{ error.message }}</section>
    <section v-else>
      <ul class="grid grid-cols-1 gap-4">
        <li v-for="project in projects" :key="project.id" class="text-slate-500 border-gray-200 rounded-md p-2 hover:bg-gray-100 font-mono border-2">
          <a :href="project.html_url" target="_blank">
            <div class="flex items-center justify-between">
              <div class="font-semibold text-sm">{{ project.name }}</div>
              <div class="text-xs text-gray-500">{{ project.language }}</div>
            </div>
            <p class="text-sm">{{ project.description }}</p>
          </a>
        </li>
      </ul>
    </section>
    
  </div>
</template>

<script lang="ts" setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/nortonx/repos')

const projects = computed(() => {
  return data.value.filter((project: any) => project.description)
})
</script>
