<template>
  <section class="mt-14 scroll-mt-24">
    <div class="text-center">
      <h2 class="text-3xl font-black sm:text-4xl">Portfolio</h2>
      <p class="mx-auto mt-3 max-w-2xl text-base text-zinc-300">
        Explore my journey through projects and certifications.
      </p>
    </div>

    <!-- Tab Switcher -->
    <div class="mt-8">
      <div class="mx-auto max-w-6xl rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-3 sm:p-4 shadow-soft">
        <div class="grid gap-3 sm:grid-cols-2">
          <button
            v-for="tab in tabs"
            :key="tab.id"
            @click="activeTab = tab.id"
            :class="[
              'cursor-pointer rounded-[1.6rem] border border-white/10 bg-white/[0.04] px-5 py-4 text-center text-sm font-semibold text-zinc-300 transition hover:bg-white/10',
              activeTab === tab.id ? 'border-white/15 bg-white/[0.08] text-white' : ''
            ]">
            <span class="inline-flex items-center justify-center gap-2">
              <span class="opacity-80">{{ tab.icon }}</span>
              {{ tab.label }}
            </span>
          </button>
        </div>
      </div>

      <!-- Projects Panel -->
      <div v-show="activeTab === 'projects'" id="projects" class="scroll-mt-24 mt-6">
        <div class="grid gap-4 md:grid-cols-2 lg:grid-cols-3">
          <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
        </div>
      </div>

      <!-- Certificates Panel -->
      <div v-show="activeTab === 'certs'" id="certificates" class="scroll-mt-24 mt-6">
        <div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
          <CertificateCard v-for="cert in certificates" :key="cert.title" :cert="cert" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProjectCard from './ProjectCard.vue'
import CertificateCard from './CertificateCard.vue'

const activeTab = ref('projects')

const tabs = [
  { id: 'projects', label: 'Projects', icon: '📁' },
  { id: 'certs', label: 'Certifications', icon: '🏅' },
]

const projects = [
  {
    title: 'Ziontech Communication Inc.',
    role: 'as a Developer',
    description: 'The ZionTech Communication website serves as a simple landing page designed to introduce the company and services offered. It provides visitors with a quick overview of ZionTech, including core services, contact information, and ways to reach out.',
    image: 'https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Github', variant: 'default' },
      { label: 'Tailwind CSS', variant: 'accent' },
      { label: 'JavaScript', variant: 'default' },
      { label: 'Hostinger', variant: 'accent' },
    ],
  },
  {
    title: 'Innovence I.T Services',
    role: 'as a Developer',
    description: 'The Innovence I.T. Services landing page gives visitors a clear introduction to the company and the technology solutions provided. The site highlights a commitment to delivering smart, reliable, and efficient IT services.',
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Tailwind', variant: 'default' },
      { label: 'JS', variant: 'default' },
      { label: 'Responsive', variant: 'accent' },
    ],
  },
  {
    title: 'Z-Kiosk Pro Queueing System',
    role: 'as a Quality Assurance / Tester',
    description: 'Multi-department queue, priority handling, real-time monitoring UI.',
    image: 'https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Tailwind', variant: 'default' },
      { label: 'JS', variant: 'default' },
      { label: 'Responsive', variant: 'accent' },
    ],
  },
  {
    title: 'Konekta 670 Barangay System',
    role: 'as a Front-End Developer',
    description: 'Multi-department queue, priority handling, real-time monitoring UI.',
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Tailwind', variant: 'default' },
      { label: 'JS', variant: 'default' },
      { label: 'Responsive', variant: 'accent' },
    ],
  },
  {
    title: 'Health Me!',
    role: 'as a Mobile App Developer',
    description: 'The Health Me! web and mobile app was developed to support rehabilitation for patients with mild musculoskeletal conditions through gamification. Findings show the system effectively improves patient motivation and therapy adherence.',
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Tailwind', variant: 'default' },
      { label: 'JS', variant: 'default' },
      { label: 'Responsive', variant: 'accent' },
    ],
  },
  {
    title: 'Personal Portfolio',
    role: 'as a Developer',
    description: "Hi! I'm Jessie, an aspiring IT professional with a passion for tech, design, and problem-solving. This portfolio was built to showcase projects, skills, and the journey in the world of technology.",
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=1200&auto=format&fit=crop',
    tags: [
      { label: 'Tailwind', variant: 'default' },
      { label: 'JS', variant: 'default' },
      { label: 'Responsive', variant: 'accent' },
    ],
  },
]

const certificates = [
  { title: 'Introduction to Front-End Development (Meta)', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
  { title: 'Reactjs - The Complete ReactJs Course For Beginners', year: '2025', description: 'Complete React course covering components, hooks, and state.' },
  { title: 'Web Development', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
  { title: 'Front-end for Beginners', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
  { title: 'Programming with Javascript (Meta)', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
  { title: 'Introduction to CSS', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
  { title: 'Introduction to HTML', year: '2025', description: 'HTML, CSS, JavaScript fundamentals and quizzes.' },
]
</script>