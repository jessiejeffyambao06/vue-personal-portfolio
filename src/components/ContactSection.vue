<template>
  <section id="contact" class="mt-14 scroll-mt-24">
    <div class="text-center">
      <h2 class="mt-2 text-3xl font-black sm:text-4xl">Let's talk.</h2>
      <p class="mx-auto mt-3 max-w-2xl text-base text-zinc-300">
        A cleaner, more modern contact layout.
      </p>
    </div>

    <div class="mt-8 grid gap-6 lg:grid-cols-[0.95fr_1.05fr] lg:items-start">

      <!-- Contact Info -->
      <div class="grid gap-4">
        <div class="rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-6 sm:p-7 shadow-soft">
          <div class="flex items-start gap-4">
            <span class="grid h-12 w-12 place-items-center rounded-2xl border border-emerald-400/25 bg-emerald-500/10">
              <svg class="h-6 w-6 text-emerald-200" viewBox="0 0 24 24" fill="none">
                <path d="M4 6.5l8 6 8-6" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                <path d="M5 7.5v10A2.5 2.5 0 0 0 7.5 20h9A2.5 2.5 0 0 0 19 17.5v-10" stroke="currentColor" stroke-width="2"/>
              </svg>
            </span>
            <div class="min-w-0">
              <p class="text-xs text-zinc-400">Email</p>
              <p class="mt-1 text-base font-semibold text-white break-words">jessiejeffyambao06@gmail.com</p>
            </div>
          </div>
        </div>

        <div class="rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-6 sm:p-7 shadow-soft">
          <div class="flex items-start gap-4">
            <span class="grid h-12 w-12 place-items-center rounded-2xl border border-blue-400/25 bg-blue-500/10">
              <svg class="h-6 w-6 text-blue-200" viewBox="0 0 24 24" fill="none">
                <path d="M12 12a5 5 0 1 0-5-5 5 5 0 0 0 5 5Z" stroke="currentColor" stroke-width="2"/>
                <path d="M20 21a8 8 0 1 0-16 0" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </span>
            <div class="min-w-0">
              <p class="text-xs text-zinc-400">Contact No.</p>
              <p class="mt-1 text-base font-semibold text-white">+63 951 474 1849</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <div class="relative overflow-hidden rounded-[2.2rem] border border-white/10 bg-white/[0.05] p-6 sm:p-7 backdrop-blur-xl shadow-neon">
        <div aria-hidden="true" class="absolute -inset-24 bg-gradient-to-r from-blue-500/12 via-transparent to-rose-500/10 blur-2xl"></div>

        <div class="relative">
          <p class="text-base font-semibold text-white">Send a message</p>

          <div class="mt-6 grid gap-4">
            <div class="grid gap-4 sm:grid-cols-2">
              <div>
                <label class="text-xs text-zinc-400" for="name">Name</label>
                <input
                  id="name" v-model="form.name" type="text" placeholder="Your name"
                  class="mt-2 w-full rounded-3xl border border-white/10 bg-zinc-950/40 px-4 py-3 text-base text-white placeholder:text-zinc-600 outline-none focus:border-emerald-400/55 focus:ring-2 focus:ring-emerald-400/20" />
              </div>
              <div>
                <label class="text-xs text-zinc-400" for="email">Email</label>
                <input
                  id="email" v-model="form.email" type="email" placeholder="you@email.com"
                  class="mt-2 w-full rounded-3xl border border-white/10 bg-zinc-950/40 px-4 py-3 text-base text-white placeholder:text-zinc-600 outline-none focus:border-blue-400/55 focus:ring-2 focus:ring-blue-400/20" />
              </div>
            </div>

            <div>
              <label class="text-xs text-zinc-400" for="topic">Topic</label>
              <input
                id="topic" v-model="form.topic" type="text" placeholder="e.g., Portfolio, Website, System UI"
                class="mt-2 w-full rounded-3xl border border-white/10 bg-zinc-950/40 px-4 py-3 text-base text-white placeholder:text-zinc-600 outline-none focus:border-fuchsia-400/55 focus:ring-2 focus:ring-fuchsia-400/20" />
            </div>

            <div>
              <label class="text-xs text-zinc-400" for="message">Message</label>
              <textarea
                id="message" v-model="form.message" rows="6" placeholder="Tell me about your project..."
                class="mt-2 w-full resize-none rounded-3xl border border-white/10 bg-zinc-950/40 px-4 py-3 text-base text-white placeholder:text-zinc-600 outline-none focus:border-yellow-400/55 focus:ring-2 focus:ring-yellow-400/20">
              </textarea>
            </div>

            <button
              type="button"
              @click="handleSubmit"
              class="relative inline-flex items-center justify-center rounded-3xl bg-white px-6 py-3 text-sm font-semibold text-zinc-900 hover:bg-zinc-100 overflow-hidden transition">
              <span aria-hidden="true" class="absolute -left-1/2 top-0 h-full w-1/2 bg-zinc-200/40 rotate-12 animate-shimmer"></span>
              <span class="relative">Send Message</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  topic: '',
  message: '',
})

function handleSubmit() {
  // TODO: wire up your email/backend service here
  console.log('Form submitted:', { ...form })
  alert('Message sent! (connect to backend to complete)')
}
</script>