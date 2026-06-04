---
layout: default
---

# Flow Field Visualizations

<div style="display:grid; grid-template-columns:repeat(3,1fr); gap:0 1rem; margin-top:0.25rem;">
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 4px">Pressure</div>
    <video :src="'/assets/media/07_pressure_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 6px">z-midplane</div>
    <video :src="'/assets/media/08_pressure_x_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 0">x-midplane</div>
  </div>
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 4px">Velocity Magnitude</div>
    <video :src="'/assets/media/03_velocity_mag_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 6px">z-midplane</div>
    <video :src="'/assets/media/04_velocity_mag_x_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 0">x-midplane</div>
  </div>
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 4px">Q-Criterion</div>
    <video :src="'/assets/media/01_q_criterion_z_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 6px">z-midplane</div>
    <video :src="'/assets/media/02_q_criterion_x_midplane.webm'" autoplay loop muted playsinline class="rounded w-full" style="height:175px; object-fit:contain; display:block" />
    <div class="text-xs opacity-50" style="margin:2px 0 0">x-midplane</div>
  </div>
</div>
