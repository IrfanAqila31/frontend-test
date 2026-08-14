<script setup lang="ts">
import NavbarComponent from './components/NavbarComponent.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import TestimoniSection from './components/TestimoniSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterComponent from './components/FooterComponent.vue'
</script>

<template>
  <header>
    <NavbarComponent />
  </header>
  <main>
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <TestimoniSection />
    <ContactSection />
  </main>
  <footer>
    <FooterComponent />
  </footer>
</template>

<style scoped></style>
