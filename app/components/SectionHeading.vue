<script setup lang="ts">
defineProps<{ title: string; subtitle?: string }>()
</script>

<template>
  <div class="mb-10 max-w-2xl">
    <h2 class="font-display text-3xl font-bold tracking-tight sm:text-4xl">{{ title }}</h2>
    <div class="mt-3 h-1 w-20 rounded-full bg-ember-gradient" />
    <p v-if="subtitle" class="mt-4 text-ash">{{ subtitle }}</p>
  </div>
</template>