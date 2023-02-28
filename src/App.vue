<script>
// import MainHeader from './components/MainHeader.vue'
// import HeroSection from './components/HeroSection.vue'
// import ServicesSection from './components/ServicesSection.vue'
// import AboutSection from './components/AboutSection.vue'
// import ReferenceSection from './components/ReferenceSection.vue'
// import ContactSection from './components/ContactSection.vue'
// import FooterSection from './components/FooterSection.vue'
// import HomeImage from '@/assets/images/home-image.jpg'
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
