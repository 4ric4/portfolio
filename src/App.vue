
<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <ExperienceAndSkills />
    <LatestProjSecstion />

  </div>

</template>


<script setup>
import { defineAsyncComponent } from 'vue'
const NavBar = defineAsyncComponent(() => import('@/components/NavBar.vue'))
const HeroSection = defineAsyncComponent(() => import('@/components/HeroSection.vue'))
const ServicesSection = defineAsyncComponent(() => import('@/components/ServicesSection.vue'))
const AboutSection = defineAsyncComponent(() => import('@/components/AboutSection.vue'))
const ExperienceAndSkills = defineAsyncComponent(() => import('@/components/ExperienceAndSkills.vue'))
const LatestProjSecstion = defineAsyncComponent(() => import('@/components/LatestProjSecstion.vue'))

</script>