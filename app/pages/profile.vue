<script setup lang="ts">
import { profile as p } from '~/data/profile'

useHead({ title: 'Profile | Ermi Shayne P. Cagadas' })
</script>

<template>
  <div class="mx-auto max-w-6xl px-5 pb-24 pt-12 sm:pt-16">
    <section class="grid items-end gap-10 md:grid-cols-[20rem_1fr] md:gap-16">
      <div class="mx-auto w-full max-w-[18rem] md:max-w-none">
        <ProfileAvatar :src="p.photo" alt="Profile photo" />
      </div>

      <div class="pb-2 md:pb-12">
        <h1 class="font-display text-4xl font-extrabold tracking-tight sm:text-5xl">
          <span class="text-gradient">{{ p.fullName }}</span>
        </h1>
        <p class="mt-6 max-w-2xl text-xl leading-relaxed text-bone/90">{{ p.about }}</p>

        <div class="mt-8">
          <h2 class="text-sm font-semibold text-honey">What I value</h2>
          <ul class="mt-3 flex flex-wrap gap-x-7 gap-y-2 text-lg">
            <li v-for="v in p.values" :key="v" class="flex items-center gap-2.5">
              <span class="h-1.5 w-1.5 rounded-full bg-ember" aria-hidden="true" />
              {{ v }}
            </li>
          </ul>
        </div>

      </div>
    </section>

    <ProfileSection id="education" title="Education" class="mt-0!">
      <p class="font-display text-2xl font-bold sm:text-3xl">{{ p.education.school }}</p>
      <p class="mt-1 text-ash">{{ p.education.college }}</p>
      <p class="mt-4 text-lg text-honey">
        {{ p.education.program }}
        <span class="text-ash"> &ndash; {{ p.education.year }}</span>
      </p>
      <p class="mt-6 max-w-2xl leading-relaxed text-bone/80">{{ p.education.story }}</p>
    </ProfileSection>

    <ProfileSection id="skills" title="Skills and Interests">
      <p class="max-w-2xl italic text-ash">{{ p.skillsNote }}</p>
      <div class="mt-8 grid gap-10 sm:grid-cols-2 lg:grid-cols-3">
        <SkillGroup title="Technical skills" :items="p.technical" />
        <SkillGroup title="Personal skills" :items="p.personalSkills" />
        <SkillGroup title="Areas of interest" :items="p.interests" />
      </div>
    </ProfileSection>

    <ProfileSection id="hobbies" title="Hobbies and Personal Interests">
      <div class="grid gap-5 sm:grid-cols-2 lg:grid-cols-3">
        <HobbyCard v-for="h in p.hobbies" :key="h.title" v-bind="h" />
      </div>
    </ProfileSection>
  </div>
</template>
