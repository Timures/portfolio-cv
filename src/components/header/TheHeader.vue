<script setup>
import TheLogo from './TheLogo.vue'
import TheNavbar from './TheNavbar.vue'
import HamburgerMenu from './HamburgerMenu.vue'
</script>

<template>
    <header class="header">
    <TheLogo />
    <TheNavbar />
    <HamburgerMenu />
  </header>
</template>

<style lang="scss">
.header {
    max-width: 1280px;
    margin: 0 auto;
  padding: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  @media screen and (max-width: 768px) {
    padding: 1rem;
  }
}
</style>