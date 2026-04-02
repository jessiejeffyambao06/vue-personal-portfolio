<template>
  <section id="services" class="mt-14 scroll-mt-24">
    <div class="text-center">
      <h2 class="mt-2 text-3xl font-black sm:text-4xl">Services Offered.</h2>
    </div>

    <div class="mt-8 grid gap-4 lg:grid-cols-3">
      <article
        v-for="service in services"
        :key="service.title"
        :class="[
          'group rounded-[2.2rem] border bg-white/[0.05] p-6 sm:p-7 shadow-soft hover:bg-white/10 transition',
          service.featured
            ? 'border-emerald-400/25 shadow-neon relative overflow-hidden'
            : 'border-white/10'
        ]">

        <!-- Hover glow for featured -->
        <div v-if="service.featured"
          class="pointer-events-none absolute inset-0 opacity-0 group-hover:opacity-100 transition">
          <div class="absolute -inset-24 bg-gradient-to-r from-emerald-500/14 via-transparent to-yellow-500/10 blur-2xl"></div>
        </div>

        <div :class="['flex items-start justify-between gap-3', service.featured ? 'relative' : '']">
          <span :class="`grid h-12 w-12 place-items-center rounded-2xl border ${service.iconBorder} ${service.iconBg}`">
            <svg class="h-6 w-6" :class="service.iconColor" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path v-for="(p, i) in service.paths" :key="i" v-bind="p" />
            </svg>
          </span>
          <span :class="[
            'rounded-full border px-3 py-1 text-xs',
            service.featured
              ? 'border-emerald-400/25 bg-emerald-500/10 font-semibold text-emerald-200 relative'
              : 'border-white/10 bg-white/[0.05] text-zinc-300'
          ]">
            {{ service.badge }}
          </span>
        </div>

        <h3 :class="['mt-6 text-2xl font-semibold', service.featured ? 'relative text-emerald-200' : 'text-blue-200']">
          {{ service.title }}
        </h3>
        <p :class="['mt-2 text-base text-zinc-300', service.featured ? 'relative' : '']">
          {{ service.description }}
        </p>
      </article>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: 'Site Maintenance',
    description: 'Keep your website up-to-date, fast, and secure with regular updates and technical support.',
    badge: 'Design',
    featured: false,
    iconBorder: 'border-blue-400/25',
    iconBg: 'bg-blue-500/10',
    iconColor: 'text-blue-200',
    paths: [
      { d: 'M4 6h16M4 10h10M4 14h16M4 18h10', stroke: 'currentColor', 'stroke-width': '2', 'stroke-linecap': 'round' },
    ],
  },
  {
    title: 'Custom System UI',
    description: 'Create smooth user experiences using tools like Figma and Canva with a focus on accessibility.',
    badge: 'Featured',
    featured: true,
    iconBorder: 'border-emerald-400/25',
    iconBg: 'bg-emerald-500/10',
    iconColor: 'text-emerald-200',
    paths: [
      { d: 'M7 7h10v10H7V7Z', stroke: 'currentColor', 'stroke-width': '2' },
      { d: 'M5 12H3M21 12h-2M12 5V3M12 21v-2', stroke: 'currentColor', 'stroke-width': '2', 'stroke-linecap': 'round' },
    ],
  },
  {
    title: 'Website Development',
    description: 'I build responsive websites using modern HTML, CSS, JS, and frameworks like React.',
    badge: 'Build',
    featured: false,
    iconBorder: 'border-blue-400/25',
    iconBg: 'bg-blue-500/10',
    iconColor: 'text-blue-200',
    paths: [
      { d: 'M4 7h16M4 12h16M4 17h16', stroke: 'currentColor', 'stroke-width': '2', 'stroke-linecap': 'round' },
      { d: 'M9 7v10', stroke: 'currentColor', 'stroke-width': '2', 'stroke-linecap': 'round' },
    ],
  },
]
</script>