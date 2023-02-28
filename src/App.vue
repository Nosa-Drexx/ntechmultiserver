<script>
import LandingPage from '@/views/LandingPage/LandingPage.vue'
export default {
  components: {
    LandingPage
  }
}
</script>

<template>
  <LandingPage />
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}
html {
  box-sizing: border-box;
  scroll-behavior: smooth;
}
body {
  margin: 0;
  padding: 0;
  background: var(--white);
}
</style>
