<script setup lang="ts">
import { profile } from '~/data/profile'

useHead({ title: 'Home | Ermi Shayne P. Cagadas' })
</script>

<template>
  <section>
    <div
      class="mx-auto grid max-w-6xl items-end gap-8 px-5 md:min-h-[calc(100svh-4rem)] md:grid-cols-[1fr_1.1fr]"
    >
      <div class="self-center py-14">
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

      <div class="rise rise-2 mx-auto w-full max-w-sm sm:max-w-md md:max-w-none">
        <ProfileAvatar :src="profile.photo" alt="Profile photo" />
      </div>
    </div>

    <!-- Divider the photo stands on, leading into the footer -->
    <div class="h-px bg-gradient-to-r from-transparent via-burnt/50 to-ember" />
  </section>
</template>
