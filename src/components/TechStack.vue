<template>
  <section id="stack" class="mt-10 scroll-mt-24">
    <div class="relative edge-fade marquee overflow-hidden rounded-[2.2rem] border border-white/10 bg-white/[0.04] p-4 sm:p-5 shadow-neon">
      <div class="marquee-track flex w-[200%] items-center gap-3 sm:gap-4 animate-marqueeR">
        <!-- Render two groups for seamless loop -->
        <div v-for="group in 2" :key="group" class="flex shrink-0 w-max items-center gap-3 sm:gap-4 pr-4">
          <div
            v-for="tech in techItems"
            :key="`${group}-${tech.name}`"
            class="shrink-0 min-w-[150px] sm:min-w-[170px] rounded-2xl border border-white/10 bg-white/[0.05] px-4 py-3">
            <div class="flex items-center gap-3">
              <span :class="`grid h-9 w-9 place-items-center rounded-xl border ${tech.borderColor} ${tech.bgColor}`">
                <img class="h-6 w-6" :alt="tech.name" :src="tech.icon" :style="tech.invert ? 'filter: invert(1)' : ''" />
              </span>
              <span class="whitespace-nowrap text-sm font-semibold text-zinc-200">{{ tech.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const techItems = [
  { name: 'HTML',       icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg',           borderColor: 'border-blue-400/25',    bgColor: 'bg-blue-500/10',     invert: false },
  { name: 'CSS',        icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg',             borderColor: 'border-emerald-400/25', bgColor: 'bg-emerald-500/10',  invert: false },
  { name: 'JavaScript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg', borderColor: 'border-yellow-400/25',  bgColor: 'bg-yellow-500/10',   invert: false },
  { name: 'Tailwind',   icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg',borderColor: 'border-cyan-400/25',    bgColor: 'bg-cyan-500/10',     invert: false },
  { name: 'React',      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg',           borderColor: 'border-blue-400/25',    bgColor: 'bg-blue-500/10',     invert: false },
  { name: 'GitHub',     icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg',         borderColor: 'border-zinc-400/20',    bgColor: 'bg-white/5',         invert: false },
  { name: 'Git',        icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg',               borderColor: 'border-rose-400/25',    bgColor: 'bg-rose-500/10',     invert: false },
  { name: 'Figma',      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg',           borderColor: 'border-fuchsia-400/25', bgColor: 'bg-fuchsia-500/10',  invert: false },
  { name: 'MySQL',      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg',           borderColor: 'border-amber-400/25',   bgColor: 'bg-amber-500/10',    invert: false },
  { name: 'XAMPP',      icon: 'https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/xampp.svg',                         borderColor: 'border-orange-400/25',  bgColor: 'bg-orange-500/10',   invert: true  },
  { name: 'GoDaddy',    icon: 'https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/godaddy.svg',                       borderColor: 'border-orange-400/25',  bgColor: 'bg-orange-500/10',   invert: true  },
  { name: 'Vercel',     icon: 'https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/vercel.svg',                        borderColor: 'border-white/10',       bgColor: 'bg-white/5',         invert: true  },
  { name: 'Hostinger',  icon: 'https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/hostinger.svg',                     borderColor: 'border-emerald-400/25', bgColor: 'bg-emerald-500/10',  invert: true  },
]
</script>