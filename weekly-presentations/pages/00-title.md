---
layout: default
background: /assets/backgrounds/bg1.jpg
colorSchema: dark
---

<div class="absolute inset-0" style="background-color:#0F3D24"></div>

<div class="relative h-full flex flex-col px-16 py-10 text-white">

  <div class="text-xs tracking-widest uppercase opacity-50 self-end">
    General Presentation - 2026
  </div>

  <div class="flex-1 flex flex-col justify-center">
    <div class="w-14 h-1 bg-primary mb-8"></div>
    <h1 class="text-4xl font-bold leading-snug mb-10" style="color:#F5A800">
      Introducing OvrFlw: <br>
      an AMReX-Based Solver for Exa-Scale Simulation of Incompressible Flows
    </h1>
    <div class="space-y-3 text-base">
      <div>
        <p class="font-semibold">Thien-Tam Nguyen &amp; Dr. Trung B. Le</p>
        <p class="text-sm opacity-60">Dept. of Civil, Construction &amp; Environmental Engineering · North Dakota State University</p>
      </div>
      <div>
        <p class="font-semibold">Dr. Andy Nonaka</p>
        <p class="text-sm opacity-60">Center for Computational Sciences and Engineering · Lawrence Berkeley National Laboratory</p>
      </div>
    </div>
  </div>

  <div class="border-t border-white/20 pt-5 flex items-center gap-8">
    <!-- Institution logos. Replace each placeholder div with:
         <img :src="'/assets/logos/logo-name.png'" class="h-8 brightness-0 invert opacity-80" alt="Institution" />
         - :src (not src) — avoids Vite's static import resolver
         - brightness-0 invert — forces logo white (title slide is always dark)
         - For slides with variable backgrounds use dark:brightness-0 dark:invert instead
         Logos tile automatically — just add or remove items. -->
    <img :src="'/assets/logos/NDSU.png'" class="h-6 brightness-0 invert opacity-80" alt="NDSU" />
    <img :src="'/assets/logos/LBNL.png'" class="h-8 brightness-0 invert opacity-80" alt="LBNL" />
    <img :src="'/assets/logos/NSFNSB.png'" class="h-12 brightness-0 invert opacity-80" alt="NSF" />
  </div>

</div>
