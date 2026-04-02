<template>
  <!-- Background -->
  <AppBackground />

  <!-- Navbar -->
  <AppNavbar />

  <!-- Main Content -->
  <main id="home" class="mx-auto max-w-6xl px-4 py-10 md:px-6 md:py-12">
    <HeroSection />
    <TechStack />
    <ExperienceSection />
    <ServicesSection />
    <PortfolioSection />
    <QuoteSection />
    <ContactSection />
  </main>

  <!-- Footer -->
  <AppFooter />
</template>

<script setup>
import AppBackground from './components/AppBackground.vue'
import AppNavbar from './components/AppNavbar.vue'
import HeroSection from './components/HeroSection.vue'
import TechStack from './components/TechStack.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import PortfolioSection from './components/PortfolioSection.vue'
import QuoteSection from './components/QuoteSection.vue'
import ContactSection from './components/ContactSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>