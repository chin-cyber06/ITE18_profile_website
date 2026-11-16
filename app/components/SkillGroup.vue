<script setup lang="ts">
defineProps<{ title: string; items: string[] }>()
</script>

<template>
  <div>
    <h3 class="text-sm font-semibold text-honey">{{ title }}</h3>
    <ul class="mt-3 divide-y divide-smoke border-t border-smoke">
      <li
        v-for="i in items"
        :key="i"
        class="flex items-start gap-3 py-2.5 text-bone/90 transition duration-300 hover:text-honey"
      >
        <span class="mt-[0.7rem] h-1 w-1 shrink-0 rounded-full bg-ember" aria-hidden="true" />
        {{ i }}
      </li>
    </ul>
  </div>
</template>
