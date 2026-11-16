<script setup lang="ts">
defineProps<{ icon: string; title: string; text: string }>()
</script>

<template>
  <div
    class="group rounded-3xl border border-white/10 bg-graphite p-6 transition duration-300 hover:-translate-y-1 hover:border-ember/60 hover:bg-gradient-to-br hover:from-graphite hover:to-burnt/30"
  >
    <div class="grid h-12 w-12 place-items-center rounded-2xl bg-ember/15 text-2xl transition group-hover:scale-110">
      {{ icon }}
    </div>
    <h3 class="mt-4 font-display text-lg font-bold">{{ title }}</h3>
    <p class="mt-1 text-sm text-ash">{{ text }}</p>
  </div>
</template>