<script setup lang="ts">
import { profile } from '~/data/profile'

useHead({ title: 'Home | Ermi Shayne P. Cagadas' })
</script>

<template>
  <section class="mx-auto grid min-h-[calc(100vh-4rem)] max-w-6xl items-center gap-12 px-5 py-14 md:grid-cols-[1.45fr_1fr]">
    <div>
      <p class="rise text-sm font-medium text-honey">Hello, I'm</p>
      <h1 class="rise rise-2 mt-3 font-display text-5xl font-extrabold leading-[1.02] tracking-tight sm:text-6xl lg:text-7xl">
        <span class="text-gradient">{{ profile.displayName }}</span>
      </h1>
      <p class="rise rise-3 mt-6 max-w-xl text-lg leading-relaxed text-ash">{{ profile.intro }}</p>

      <div class="rise rise-3 mt-10 max-w-xl border-l-2 border-ember pl-5">
        <h2 class="font-display text-xl font-bold">{{ profile.welcomeTitle }}</h2>
        <p class="mt-2 leading-relaxed text-bone/75">{{ profile.welcomeText }}</p>
      </div>

      <div class="rise rise-3 mt-8">
        <AppButton to="/profile">Explore My Profile</AppButton>
      </div>
    </div>

    <div class="rise rise-2 mx-auto w-64 sm:w-72 md:w-full md:max-w-sm">
      <ProfileAvatar :src="profile.photo" alt="Profile photo" />
    </div>
  </section>
</template>
