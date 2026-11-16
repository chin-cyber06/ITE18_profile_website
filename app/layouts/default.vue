<template>
  <div class="relative flex min-h-screen flex-col overflow-x-hidden bg-ink">
    <div class="pointer-events-none absolute -right-40 -top-40 h-[32rem] w-[32rem] rounded-full bg-ember/20 blur-[120px]" aria-hidden="true" />
    <div class="pointer-events-none absolute -left-52 top-[55rem] h-[28rem] w-[28rem] rounded-full bg-burnt/15 blur-[120px]" aria-hidden="true" />
    <AppNavbar />
    <main class="relative flex-1 pt-16">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>
