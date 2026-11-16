<script setup lang="ts">
import { profile } from '~/data/profile'

const year = new Date().getFullYear()
</script>

<template>
  <footer class="border-t border-white/5 bg-coal">
    <div class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-3 px- py-8 text-sm text-ash sm:flex-row">
      <p>&copy; {{ year }} {{ profile.fullName }}. All rights reserved.</p>
      <p class="italic text-honey/80">"{{ profile.motto }}"</p>
    </div>
  </footer>
</template>