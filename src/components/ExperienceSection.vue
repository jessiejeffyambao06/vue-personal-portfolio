<template>
  <section id="experience" class="mt-14 scroll-mt-24">
    <div class="flex flex-col gap-2 text-center">
      <h2 class="text-2xl font-black sm:text-4xl mb-6">Career Timeline.</h2>
    </div>

    <div class="relative overflow-hidden rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-6 sm:p-7 shadow-soft">
      <!-- Center line (desktop) -->
      <div class="pointer-events-none absolute left-1/2 top-24 hidden h-[calc(100%-7.5rem)] w-px -translate-x-1/2 bg-white/10 lg:block"></div>

      <div class="mt-8 grid gap-7">
        <TimelineItem
          v-for="(item, i) in timeline"
          :key="i"
          :item="item"
          :align="i % 2 === 0 ? 'left' : 'right'"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import TimelineItem from './TimelineItem.vue'

const timeline = [
  {
    date: 'June 2025 - Present',
    title: 'IT Support Specialist',
    company: 'Ziontech Communication Inc.',
    description: 'Maintained and deployed company websites, developed client-facing front-end systems, and performed QA testing for QMS platforms. Assisted in infrastructure implementations including kiosk deployment, structured cabling, CCTV installation, data center site assessments. Worked alongside the sales team during client meetings and site inspections, and handled hardware and network troubleshooting within the organization.',
    theme: 'blue',
  },
  {
    date: 'March 2025 — June 2025',
    title: 'Software Engineer Intern',
    company: 'Ziontech Communication Inc.',
    description: 'Developed landing pages for internal and client projects, supported kiosk system deployment and OS installation, and performed hardware evaluation to verify compliance with client technical requirements before acquisition.',
    theme: 'white',
  },
  {
    date: 'October 2021 - October 2025',
    title: 'Bachelor of Science in Information Technology',
    company: 'Polytechnic University of the Philippines',
    description: 'Health Me! - Built a gamified rehabilitation tracking solution that enables patient progress monitoring through a mobile application and an integrated admin management system.',
    theme: 'blue',
  },
]
</script>