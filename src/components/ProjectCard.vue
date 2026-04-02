<template>
  <article class="group overflow-hidden rounded-[2.2rem] border border-white/10 bg-white/[0.05] hover:bg-white/10 transition shadow-soft">

    <!-- Image Header -->
    <div class="relative h-44 w-full overflow-hidden">
      <img
        :src="project.image"
        :alt="`${project.title} preview`"
        class="h-full w-full object-cover opacity-80 transition duration-500 group-hover:scale-105"
        loading="lazy"
      />
      <div class="absolute inset-0 bg-gradient-to-t from-zinc-950 via-zinc-950/40 to-transparent"></div>
      <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition">
        <div class="absolute -left-1/2 top-0 h-full w-1/2 bg-white/12 rotate-12 animate-shimmer"></div>
      </div>
      <div class="absolute left-4 top-4 rounded-full border border-white/10 bg-zinc-950/40 px-3 py-1 text-xs text-zinc-200 backdrop-blur">
        Web
      </div>
    </div>

    <!-- Content -->
    <div class="p-6 sm:p-7">
      <h3 class="text-lg font-semibold">{{ project.title }}</h3>
      <p class="mt-2 text-base text-blue-400">{{ project.role }}</p>
      <p class="mt-2 text-base text-zinc-300">{{ project.description }}</p>

      <div class="mt-4 flex flex-wrap gap-2 text-sm">
        <span
          v-for="tag in project.tags"
          :key="tag.label"
          :class="[
            'rounded-full border px-4 py-1.5',
            tag.variant === 'accent'
              ? 'border-emerald-400/25 bg-emerald-500/10 font-semibold text-emerald-200'
              : 'border-white/10 bg-white/[0.05]'
          ]">
          {{ tag.label }}
        </span>
      </div>

      <div class="mt-6 flex gap-3">
        <a href="#" class="inline-flex flex-1 items-center justify-center rounded-2xl bg-white px-4 py-2.5 text-sm font-semibold text-zinc-900 hover:bg-zinc-100 transition">Live</a>
        <a href="#" class="inline-flex flex-1 items-center justify-center rounded-2xl border border-white/10 bg-white/[0.05] px-4 py-2.5 text-sm font-semibold text-white hover:bg-white/10 transition">Code</a>
      </div>
    </div>
  </article>
</template>

<script setup>
defineProps({
  project: { type: Object, required: true }
})
</script>