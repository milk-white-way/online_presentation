---
layout: default
---

# Goal & Roadmap

<p class="text-base opacity-80 !mt-1 !mb-5"><span class="font-semibold">Goal:</span> an exascale-ready incompressible flow solver as the continuum backbone of a multi-scale blood-flow framework.</p>

<div class="grid grid-cols-4 gap-3 text-sm">
  <div class="rounded-lg p-4 bg-blue-500/10 border border-blue-500/30">
    <div class="flex items-center justify-between mb-2">
      <span class="font-bold text-blue-400 text-base">Phase 1</span>
      <span class="text-xs font-semibold text-green-400 bg-green-400/10 rounded px-2 py-0.5">Done</span>
    </div>
    <ul class="space-y-1 opacity-90">
      <li>2D Navier-Stokes for incompressible flow</li>
      <li>Fractional Step Method</li>
      <li>Hybrid Staggered / Non-staggered Grid</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-green-500/10 border border-green-500/30">
    <div class="flex items-center justify-between mb-2">
      <span class="font-bold text-green-400 text-base">Phase 2</span>
      <span class="text-xs font-semibold text-green-400 bg-green-400/10 rounded px-2 py-0.5">Done</span>
    </div>
    <ul class="space-y-1 opacity-90">
      <li>Accuracy tests with benchmarks</li>
      <li>Scalability on multi-GPUs</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-yellow-500/10 border border-yellow-500/30">
    <div class="flex items-center justify-between mb-2">
      <span class="font-bold text-yellow-400 text-base">Phase 3</span>
      <span class="text-xs font-semibold text-yellow-400 bg-yellow-400/10 rounded px-2 py-0.5">Active</span>
    </div>
    <ul class="space-y-1 opacity-90">
      <li>HPC deployment (CCAST, Aurora)</li>
      <li>3D capability</li>
      <li>Multi-GPU scaling tests</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-red-500/10 border border-red-500/30">
    <div class="flex items-center justify-between mb-2">
      <span class="font-bold text-red-400 text-base">Phase 4</span>
      <span class="text-xs font-semibold text-slate-400 bg-slate-400/10 rounded px-2 py-0.5">Planned</span>
    </div>
    <ul class="space-y-1 opacity-90">
      <li>Immersed Boundary Method</li>
      <li>Dissipative Particle Dynamics</li>
      <li>Full biofluid applications</li>
    </ul>
  </div>
</div>

<div class="mt-5 text-center font-semibold text-primary">
  Flow Solver targeting Exascale Simulations
</div>
