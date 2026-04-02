<template>
  <div class="relative grid gap-4 lg:grid-cols-2 lg:gap-10">

    <!-- Spacer for right-aligned items -->
    <div v-if="align === 'right'" class="hidden lg:block"></div>

    <!-- Card wrapper -->
    <div :class="align === 'left' ? 'lg:flex lg:justify-end' : 'lg:flex lg:justify-start'">
      <div
        :class="[
          'group relative w-full max-w-xl rounded-[1.8rem] border border-white/10 bg-zinc-950/35 p-5 sm:p-6 overflow-hidden transition-all duration-300 hover:-translate-y-1 hover:shadow-xl',
        ]">

        <!-- Sliding background -->
        <span
          :class="[
            'absolute inset-0 -translate-x-full group-hover:translate-x-0 transition-transform duration-500 ease-out z-0',
            item.theme === 'blue' ? 'bg-blue-600' : 'bg-white'
          ]">
        </span>

        <div class="relative z-10">
          <p :class="['text-sm transition', item.theme === 'blue' ? 'text-zinc-400 group-hover:text-blue-100' : 'text-zinc-400 group-hover:text-zinc-500']">
            {{ item.date }}
          </p>
          <p :class="['mt-1 text-xl font-bold transition', item.theme === 'blue' ? 'text-blue-400 group-hover:text-white' : 'text-blue-500 group-hover:text-black']">
            {{ item.title }}
          </p>
          <p :class="['mt-1 text-base font-semibold transition', item.theme === 'blue' ? 'text-white group-hover:text-blue-100' : 'text-white group-hover:text-zinc-800']">
            {{ item.company }}
          </p>
          <p :class="['mt-3 text-base transition', item.theme === 'blue' ? 'text-zinc-300 group-hover:text-blue-50' : 'text-zinc-300 group-hover:text-zinc-700']">
            {{ item.description }}
          </p>
        </div>
      </div>
    </div>

    <!-- Spacer for left-aligned items -->
    <div v-if="align === 'left'" class="hidden lg:block"></div>

    <!-- Timeline dot -->
    <span class="absolute left-0 top-6 h-3 w-3 rounded-full bg-blue-400 shadow-[0_0_18px_blue] lg:left-1/2 lg:-translate-x-1/2"></span>
  </div>
</template>

<script setup>
defineProps({
  item: { type: Object, required: true },
  align: { type: String, default: 'left' },
})
</script>