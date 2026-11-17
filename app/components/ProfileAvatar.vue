<script setup lang="ts">
defineProps<{ src: string; alt: string }>()
</script>

<template>
  <div class="relative w-full">
    <!-- Orange arc behind the cutout -->
    <div
      class="absolute bottom-0 left-1/2 aspect-square w-[92%] -translate-x-1/2 rounded-full bg-gradient-to-t from-ember/60 via-burnt/25 to-transparent"
      aria-hidden="true"
    />
    <div
      class="absolute bottom-0 left-1/2 aspect-square w-[92%] -translate-x-1/2 scale-[1.08] rounded-full border border-ember/20"
      aria-hidden="true"
    />

    <!-- Cutout, anchored to the bottom edge -->
    <img
      :src="src"
      :alt="alt"
      class="relative mx-auto block max-h-[75vh] w-full object-contain object-bottom drop-shadow-[0_0_30px_rgba(255,106,0,0.2)]"
    />

    <!-- Glowing baseline the cutout stands on -->
    <div
      class="absolute -inset-x-6 bottom-0 h-px bg-gradient-to-r from-transparent via-ember to-transparent"
      aria-hidden="true"
    />
  </div>
</template>