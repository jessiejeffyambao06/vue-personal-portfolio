<script setup>
import { ref, onMounted } from 'vue'

const year = ref('')

onMounted(() => {
  year.value = new Date().getFullYear()
})
</script>

<template>
  <footer class="border-t border-white/10 bg-zinc-950/70 backdrop-blur-xl">
    <div class="mx-auto max-w-6xl px-4 py-10 md:px-6">
      <div class="flex flex-col gap-4 sm:flex-row sm:items-center sm:justify-between">
        <p class="text-base text-zinc-400">
          © {{ year }} Jessie Jeff. All rights reserved.
        </p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
/* Optional: dagdag styles kung gusto mo */
</style>