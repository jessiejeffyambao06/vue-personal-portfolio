<template>
  <section class="grid items-center gap-10 lg:grid-cols-2">
    <!-- Text -->
    <div class="space-y-7">
      <h1 class="text-[2.65rem] leading-[1.02] font-black tracking-tight sm:text-5xl sm:leading-[1.02] lg:text-6xl animate-floaty">
        Hi, I'm
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-blue-300 to-blue-200">Jessie Jeff</span>.
        <br class="hidden sm:block" />
        I build <span class="text-zinc-100">clean</span> &amp; <span class="text-zinc-100">responsive</span> Websites.
      </h1>
      <p class="max-w-xl text-base leading-relaxed text-zinc-300 sm:text-lg animate-floaty">
        Turning ideas into seamless digital experiences built with clarity, precision, and purpose.
      </p>
    </div>

    <!-- Profile Card -->
    <div class="relative animate-floaty">
      <div class="absolute -inset-1 rounded-[2.2rem] bg-gradient-to-r from-blue-500/28 via-fuchsia-500/12 to-amber-500/18 blur-2xl"></div>

      <div class="relative rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-6 sm:p-7 backdrop-blur-xl shadow-soft">
        <!-- Header -->
        <div class="flex items-center justify-between gap-4">
          <div class="space-y-1">
            <p class="text-xs text-zinc-400">Profile</p>
            <p class="text-base font-semibold">IT Support Specialist / Front-End Web Developer</p>
          </div>
          <span class="shrink-0 rounded-full border border-white/10 bg-white/[0.05] px-3 py-1 text-xs text-zinc-300">PH • On-Site</span>
        </div>

        <!-- Photo + Stats -->
        <div class="mt-6 grid gap-6 sm:grid-cols-[200px_1fr] sm:items-center">
          <div class="relative">
            <div class="absolute -inset-1 rounded-3xl bg-gradient-to-r from-emerald-500/18 via-blue-500/14 to-rose-500/16 blur-xl"></div>
            <img
              src="../assets/images/frontpic.jpg"
              alt="Profile photo of Jessie Jeff"
              class="relative h-60 w-60 rounded-3xl border border-white/10 object-cover animate-floaty"
              loading="lazy"
            />
          </div>

          <div class="space-y-4">
            <div class="grid grid-cols-2 gap-3 text-sm animate-floaty">
              <div class="rounded-3xl border border-white/10 bg-white/[0.05] p-4">
                <p class="text-xs text-zinc-400">Experience</p>
                <p class="mt-1 text-lg font-extrabold text-white">1+ yr</p>
              </div>
              <div class="rounded-3xl border border-white/10 bg-white/[0.05] p-4">
                <p class="text-xs text-zinc-400">Projects</p>
                <p class="mt-1 text-lg font-extrabold text-white">10+</p>
              </div>
            </div>

            <div class="rounded-3xl border border-white/10 bg-white/[0.05] p-4 animate-floaty">
              <p class="text-xs text-zinc-400">Currently learning</p>
              <p class="mt-1 text-base font-semibold text-blue-200">React • Tailwind • APIs</p>
              <div class="mt-3 h-px w-full bg-gradient-to-r from-transparent via-white/10 to-transparent"></div>
              <div class="mt-3 flex flex-wrap gap-2 text-xs">
                <span class="rounded-full border border-blue-800 bg-blue-800 px-3 py-1 text-white">Manage</span>
                <span class="rounded-full border border-blue-800 bg-blue-600 px-3 py-1 text-white">Build</span>
                <span class="rounded-full border border-blue-800 bg-blue-400 px-3 py-1 text-white">Maintain</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Social Links -->
        <div class="mt-7 flex flex-wrap gap-2">
          <a v-for="social in socials" :key="social.label"
            :href="social.href"
            class="rounded-2xl border border-white/10 bg-white/[0.05] px-4 py-2 text-xs text-zinc-300 hover:bg-white/10 transition">
            {{ social.label }}
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const socials = [
  { label: 'GitHub', href: '#' },
  { label: 'LinkedIn', href: '#' },
  { label: 'Email', href: '#' },
]
</script>