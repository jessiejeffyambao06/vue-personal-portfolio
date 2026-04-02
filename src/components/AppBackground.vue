<template>
  <div aria-hidden="true" class="pointer-events-none fixed inset-0 -z-10 overflow-hidden">
    <!-- Subtle grid -->
    <div class="absolute inset-0 opacity-[0.10]
      [background-image:linear-gradient(to_right,rgba(244,244,245,0.22)_1px,transparent_1px),linear-gradient(to_bottom,rgba(244,244,245,0.22)_1px,transparent_1px)]
      bg-[size:58px_58px]"></div>

    <!-- Colorful blobs -->
    <div class="absolute -top-44 left-1/2 h-[52rem] w-[52rem] -translate-x-1/2 rounded-full bg-blue-500/16 blur-3xl animate-glow"></div>
    <div class="absolute -bottom-56 left-[-16rem] h-[44rem] w-[44rem] rounded-full bg-fuchsia-500/14 blur-3xl animate-glow"></div>
    <div class="absolute -bottom-52 right-[-14rem] h-[42rem] w-[42rem] rounded-full bg-amber-500/12 blur-3xl animate-glow"></div>

    <!-- Extra accents -->
    <div class="absolute top-[14%] left-[8%] h-[22rem] w-[22rem] rounded-full bg-emerald-500/10 blur-3xl animate-glow"></div>
    <div class="absolute top-[36%] right-[6%] h-[18rem] w-[18rem] rounded-full bg-rose-500/10 blur-3xl animate-glow"></div>
    <div class="absolute bottom-[16%] left-[26%] h-[16rem] w-[16rem] rounded-full bg-yellow-400/10 blur-3xl animate-glow"></div>

    <!-- Vignette -->
    <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_center,transparent_28%,rgba(9,9,11,0.97)_78%)]"></div>

    <!-- Scanline -->
    <div class="absolute inset-0 opacity-[0.06] [background-image:linear-gradient(to_bottom,transparent,rgba(255,255,255,0.26),transparent)] bg-[length:100%_7px]"></div>
  </div>
</template>