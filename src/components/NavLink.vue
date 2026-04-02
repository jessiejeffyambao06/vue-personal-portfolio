<template>
  <a :href="href"
    class="relative inline-flex items-center rounded-xl px-4 py-3 font-bold text-zinc-300 leading-none
    overflow-hidden transition duration-300
    before:content-[''] before:absolute before:left-0 before:top-0 before:h-[2px] before:w-full
    before:bg-blue-500 before:-translate-x-full before:transition-transform before:duration-500
    after:content-[''] after:absolute after:left-0 after:bottom-0 after:h-[2px] after:w-full
    after:bg-blue-500 after:translate-x-full after:transition-transform after:duration-500
    hover:text-white hover:before:translate-x-0 hover:after:translate-x-0">
    <slot />
  </a>
</template>

<script setup>
defineProps({ href: String })
</script>