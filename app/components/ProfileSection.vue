<script setup lang="ts">
defineProps<{ title: string; id?: string }>()
</script>

<template>
  <section :id="id" class="mt-20 sm:mt-24">
    <div class="h-px bg-gradient-to-r from-ember via-burnt/30 to-transparent" />
    <div class="grid gap-6 pt-8 md:grid-cols-[17rem_1fr] md:gap-16">
      <h2 class="font-display text-2xl font-bold tracking-tight sm:text-3xl">{{ title }}</h2>
      <div><slot /></div>
    </div>
  </section>
</template>
