---
layout: default
---

# Production Run on Aurora

<p class="text-sm opacity-75 !mt-1 !mb-3">3D lid-driven cavity at scale, enabled by an allocation from the ND-Lighthouse project</p>

<div class="grid grid-cols-6 gap-2 text-center">
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">30,000</div><div class="text-xs opacity-60">Re</div></div>
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">1024³</div><div class="text-xs opacity-60">grid cells</div></div>
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">16,384</div><div class="text-xs opacity-60">MPI ranks</div></div>
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">80,000</div><div class="text-xs opacity-60">time steps</div></div>
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">~1.9 s</div><div class="text-xs opacity-60">per step</div></div>
  <div class="rounded-lg py-2 border border-primary/30"><div class="text-lg font-bold">~2k</div><div class="text-xs opacity-60">node-hours</div></div>
</div>

<div class="grid grid-cols-3 gap-3 mt-4 text-center">
  <div>
    <video :src="'/assets/media/06_vorticity_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:230px; object-fit:contain"></video>
    <div class="text-xs opacity-60 mt-1">Vorticity · z-midplane</div>
  </div>
  <div>
    <video :src="'/assets/media/03_velocity_mag_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:230px; object-fit:contain"></video>
    <div class="text-xs opacity-60 mt-1">Velocity magnitude · z-midplane</div>
  </div>
  <div>
    <video :src="'/assets/media/01_q_criterion_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:230px; object-fit:contain"></video>
    <div class="text-xs opacity-60 mt-1">Q-criterion · z-midplane</div>
  </div>
</div>
