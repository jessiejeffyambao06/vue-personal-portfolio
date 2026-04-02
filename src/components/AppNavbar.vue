<template>
  <header class="sticky top-0 z-50 border-b border-white/10 bg-zinc-950/70 backdrop-blur-xl">
    <nav class="mx-auto flex max-w-6xl items-center justify-between px-4 py-3 md:px-6">

      <!-- Logo -->
      <a href="#home" class="group inline-flex items-center gap-3">
        <span class="text-2xl font-bold tracking-wide text-zinc-100">Personal Portfolio</span>
      </a>

      <!-- Desktop Links -->
      <div class="hidden items-center gap-1 md:flex">
        <NavLink v-for="link in navLinks" :key="link.href" :href="link.href">
          {{ link.label }}
        </NavLink>
      </div>

      <!-- Desktop CTA -->
      <div class="hidden md:flex">
        <a href="#resume"
          class="relative inline-flex items-center gap-2 rounded-2xl bg-gradient-to-l from-blue-400 via-blue-600 to-blue-800 px-4 py-2 text-xl font-semibold text-white hover:opacity-90 transition overflow-hidden">
          <span aria-hidden="true" class="absolute -left-1/2 top-0 h-full w-1/2 bg-white/12 rotate-12 animate-shimmer"></span>
          <span class="relative">Resume</span>
          <span class="relative text-white-500">→</span>
        </a>
      </div>

      <!-- Mobile hamburger -->
      <button
        @click="mobileOpen = !mobileOpen"
        class="md:hidden inline-flex cursor-pointer items-center justify-center rounded-2xl border border-white/10 bg-white/[0.05] px-3 py-2 text-sm text-zinc-100 hover:bg-white/10">
        Menu
      </button>
    </nav>

    <!-- Mobile Menu -->
    <div v-if="mobileOpen" class="md:hidden border-t border-white/10 bg-zinc-950/75 backdrop-blur-xl">
      <div class="mx-auto max-w-6xl px-4 py-3">
        <div class="grid gap-2">
          <a v-for="link in navLinks" :key="link.href"
            :href="link.href"
            @click="mobileOpen = false"
            class="rounded-xl px-3 py-2 text-sm text-zinc-300 hover:bg-white/5 hover:text-white">
            {{ link.label }}
          </a>
          <a href="#resume" class="rounded-xl px-3 py-2 text-sm text-fuchsia-200 hover:bg-white/5">Resume</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import NavLink from './NavLink.vue'

const mobileOpen = ref(false)

const navLinks = [
  { href: '#stack', label: 'Tech Stack' },
  { href: '#experience', label: 'About' },
  { href: '#services', label: 'Services' },
  { href: '#certificates', label: 'Certificates' },
  { href: '#projects', label: 'Projects' },
  { href: '#contact', label: 'Contact' },
]
</script>