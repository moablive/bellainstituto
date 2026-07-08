<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Specials from './components/Specials.vue'
import Certificates from './components/Certificates.vue'
import Clients from './components/Clients.vue'
import Contact from './components/Contact.vue'
import AppFooter from './components/Footer.vue'
import { onMounted } from 'vue'

onMounted(() => {
  if (window.AOS) {
    window.AOS.init({
      duration: 800,
      once: true,
      offset: 100
    })
  }
})
</script>

<template>
  <Navbar />
  <Hero />
  <About />
  <Services />
  <Specials />
  <Certificates />
  <Clients />
  <Contact />
  <AppFooter />
</template>
