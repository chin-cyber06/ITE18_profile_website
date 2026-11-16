<script setup lang="ts">
const route = useRoute()
const open = ref(false)

const links = [
  { label: 'Home', to: '/' },
  { label: 'Profile', to: '/profile' },
]

function isActive(to: string) {
  return route.path === to
}

watch(() => route.fullPath, () => (open.value = false))
</script>

<template>
  <header class="fixed inset-x-0 top-0 z-50 border-b border-white/5 bg-black/70 backdrop-blur-lg">
    <nav class="mx-auto flex h-16 max-w-6xl items-center justify-between px-5" aria-label="Main">
      <NuxtLink to="/" class="font-display text-lg font-extrabold tracking-tight">
        <span class="text-gradient">E.S. Cagadas</span>
      </NuxtLink>

      <ul class="hidden items-center gap-1 md:flex">
        <li v-for="l in links" :key="l.label">
          <NuxtLink
            :to="l.to"
            class="rounded-full px-4 py-2 text-sm transition duration-300 hover:text-honey"
            :class="isActive(l.to) ? 'bg-ember/15 text-honey' : 'text-ash'"
          >
            {{ l.label }}
          </NuxtLink>
        </li>
      </ul>

      <button
        class="grid h-10 w-10 place-items-center rounded-full border border-white/10 md:hidden"
        :aria-expanded="open"
        aria-label="Toggle menu"
        @click="open = !open"
      >
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
          <path v-if="!open" d="M4 7h16M4 12h16M4 17h16" />
          <path v-else d="M6 6l12 12M18 6L6 18" />
        </svg>
      </button>
    </nav>

    <ul v-if="open" class="border-t border-white/5 bg-black px-5 pb-4 md:hidden">
      <li v-for="l in links" :key="l.label">
        <NuxtLink
          :to="l.to"
          class="block rounded-xl px-3 py-3 text-ash hover:bg-ember/10 hover:text-honey"
          :class="{ 'text-honey': isActive(l.to) }"
        >
          {{ l.label }}
        </NuxtLink>
      </li>
    </ul>
  </header>
</template>
