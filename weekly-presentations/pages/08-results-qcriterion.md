---
layout: two-cols
---

# Production run on Aurora HPC Cluster

A production setup for 3D Lid-Driven Cavity was performed on Aurora thanks to the allocations from ND-Lighthouse Project

System specfications:
- Re = **30,000**
- Grid: $1024^3$
- Steps achieved: **80,000**
- Total MPI ranks: **16,384**
- Speed achieved (time per step): ~**1.9 s** / step
- Node hours used: ~**2k**

::right::

<div class="flex flex-col items-center justify-center h-full gap-1 pt-10">
  <video
    :src="'/assets/media/06_vorticity_z_midplane.webm'"
    autoplay loop muted playsinline
    class="rounded w-full"
    style="max-height:320px; object-fit:contain"
  />
  <p class="text-xs opacity-50">Vorticity · z-midplane</p>
</div>
