<template>
  <article class="group overflow-hidden rounded-[2.2rem] border border-blue-400/15 bg-white/[0.05] hover:bg-white/10 transition shadow-soft">

    <!-- Image Preview -->
    <div class="relative h-44 w-full overflow-hidden">
      <img
        src="https://images.unsplash.com/photo-1584697964358-3e14ca57658b?q=80&w=1200&auto=format&fit=crop"
        alt="Certificate Preview"
        class="h-full w-full object-cover opacity-80 group-hover:scale-105 transition duration-500"
      />
      <div class="absolute inset-0 bg-gradient-to-t from-zinc-950 via-zinc-950/40 to-transparent"></div>
      <div class="absolute left-4 top-4 rounded-full border border-blue-400/25 bg-blue-500/20 px-3 py-1 text-xs font-semibold text-blue-200 backdrop-blur">
        Certificate
      </div>
    </div>

    <!-- Content -->
    <div class="p-6 sm:p-7">
      <h3 class="text-lg font-semibold text-white">{{ cert.title }}</h3>
      <p class="mt-1 text-sm text-zinc-400">Issued: {{ cert.year }}</p>
      <p class="mt-3 text-base text-zinc-300">{{ cert.description }}</p>
      <div class="mt-6">
        <a href="#" class="inline-flex items-center gap-2 text-sm font-semibold text-blue-200 hover:text-blue-100 transition">
          View Certificate →
        </a>
      </div>
    </div>
  </article>
</template>

<script setup>
defineProps({
  cert: { type: Object, required: true }
})
</script>