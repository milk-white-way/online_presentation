---
layout: default
background: /assets/backgrounds/bg1.jpg
---

<div class="absolute inset-0 bg-gradient-to-r from-black/85 via-black/60 to-black/20"></div>

<div class="relative h-full flex flex-col px-16 py-10">

  <div class="text-xs tracking-widest uppercase opacity-50 self-end">
    Conference Name · Year
  </div>

  <div class="flex-1 flex flex-col justify-center">
    <div class="w-14 h-1 bg-primary mb-8"></div>
    <h1 class="text-4xl font-bold leading-snug mb-10">
      Presentation Title
    </h1>
    <div class="space-y-3 text-base">
      <div>
        <p class="font-semibold">Author Name(s)</p>
        <p class="text-sm opacity-60">Department · Institution</p>
      </div>
      <div>
        <p class="font-semibold">Co-author Name (if any)</p>
        <p class="text-sm opacity-60">Department · Institution</p>
      </div>
    </div>
  </div>

  <div class="border-t border-white/20 pt-5 flex items-center gap-8">
    <!-- Institution logos. Replace each placeholder div with:
         <img :src="'/assets/logos/logo-name.png'" class="h-8 brightness-0 invert opacity-80" alt="Institution" />
         - :src (not src) — avoids Vite's static import resolver
         - brightness-0 invert — forces logo white (title slide is always dark)
         - For slides with variable backgrounds use dark:brightness-0 dark:invert instead
         Logos tile automatically — add or remove items freely. -->
    <div class="border border-white/30 rounded px-3 py-1 text-xs font-bold tracking-widest opacity-60">INSTITUTION 1</div>
    <div class="border border-white/30 rounded px-3 py-1 text-xs font-bold tracking-widest opacity-60">INSTITUTION 2</div>
  </div>

</div>
