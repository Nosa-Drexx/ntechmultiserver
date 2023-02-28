<script>
import MainHeader from './components/MainHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import AboutSection from './components/AboutSection.vue'
import ReferenceSection from './components/ReferenceSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'
import HomeImage from '@/assets/images/home-image.jpg'
export default {
  components: {
    MainHeader,
    HeroSection,
    ServicesSection,
    AboutSection,
    ReferenceSection,
    ContactSection,
    FooterSection
  },
  data: () => ({
    HomeImage
  })
}
</script>

<template>
  <div class="img-background">
    <img :src="HomeImage" />
  </div>
  <div class="main-container">
    <MainHeader />
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <ReferenceSection />
    <ContactSection />
    <FooterSection />
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  align-items: center;
  flex-flow: column nowrap;
  margin: auto;
  width: 100vw;
}
.img-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: -1;
}
.img-background img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
