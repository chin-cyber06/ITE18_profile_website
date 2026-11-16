<script setup lang="ts">
withDefaults(defineProps<{ to: string; variant?: 'primary' | 'ghost' }>(), {
  variant: 'primary',
})
</script>

<template>
  <NuxtLink
    :to="to"
    class="inline-flex items-center justify-center rounded-full px-6 py-3 text-sm font-semibold transition duration-300 hover:-translate-y-0.5"
    :class="
      variant === 'primary'
        ? 'bg-ember-gradient text-black shadow-lg shadow-ember/25 hover:shadow-ember/50'
        : 'border border-ember/50 text-bone hover:border-honey hover:bg-ember/10'
    "
  >
    <slot />
  </NuxtLink>
</template>
