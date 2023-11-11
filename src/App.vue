<script setup>
import TheHeader from './components/header/TheHeader.vue'
import TheHero from './components/sections/TheHero.vue'
import TheAbout from './components/sections/TheAbout.vue'
import TheExperience from './components/sections/TheExperience.vue'
import TheProjects from './components/sections/TheProjects.vue'
import TheContact from './components/sections/TheContact.vue'
import TheFooter from './components/footer/TheFooter.vue'
</script>

<template>
  <TheHeader />
  <main class="main-content">
    <TheHero />
    <TheAbout />
    <TheExperience />
    <TheProjects />
    <TheContact />
    <TheFooter />
  </main>
</template>

<style lang="scss">
.main-content {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
}
</style>
