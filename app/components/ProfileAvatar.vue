<script setup lang="ts">
defineProps<{ src: string; alt: string }>()
</script>

<template>
  <div class="relative w-full">
    <div class="absolute -inset-5 rounded-[3rem] bg-ember/25 blur-3xl" aria-hidden="true" />
    <div class="relative rounded-[2rem] bg-gradient-to-br from-honey via-ember to-burnt p-[3px]">
      <img :src="src" :alt="alt" class="aspect-square w-full rounded-[1.85rem] bg-coal object-cover" />
    </div>
  </div>
</template>
