---
layout: default
---

# Motivations

<div class="grid grid-cols-3 gap-8 mt-10">
  <div class="border border-primary/30 rounded-lg p-6 text-center bg-primary/5">
    <div class="text-4xl mb-4">🩸</div>
    <h3 class="font-bold text-lg mb-2">Blood Plasma Modeling</h3>
    <p class="text-sm opacity-75">Simulate plasma flow behavior in complex vascular geometries</p>
  </div>
  <div class="border border-primary/30 rounded-lg p-6 text-center bg-primary/5">
    <div class="text-4xl mb-4">🔬</div>
    <h3 class="font-bold text-lg mb-2">Plasma–Cell Interaction</h3>
    <p class="text-sm opacity-75">Model interactions between plasma flow and deformable cells</p>
  </div>
  <div class="border border-primary/30 rounded-lg p-6 text-center bg-primary/5">
    <div class="text-4xl mb-4">🧫</div>
    <h3 class="font-bold text-lg mb-2">Cell Modeling</h3>
    <p class="text-sm opacity-75">Resolve cell-scale continuum mechanics at physiological conditions</p>
  </div>
</div>

<div class="mt-10 text-center text-sm opacity-60">
  Target: a flow solver capable of resolving these problems at exascale
</div>

---
layout: default
---

# Goal & Roadmap

<div class="grid grid-cols-4 gap-3 mt-6 text-sm">
  <div class="rounded-lg p-4 bg-blue-500/10 border border-blue-500/30">
    <div class="font-bold text-blue-400 mb-2 text-base">Phase 1</div>
    <ul class="space-y-1 opacity-90">
      <li>2D Navier-Stokes for incompressible flow</li>
      <li>Fractional Step Method</li>
      <li>Hybrid Staggered / Non-staggered Grid</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-green-500/10 border border-green-500/30">
    <div class="font-bold text-green-400 mb-2 text-base">Phase 2</div>
    <ul class="space-y-1 opacity-90">
      <li>Accuracy tests with benchmarks</li>
      <li>Adaptive Mesh Refinement</li>
      <li>Scalability on multi-GPUs</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-yellow-500/10 border border-yellow-500/30">
    <div class="font-bold text-yellow-400 mb-2 text-base">Phase 3</div>
    <ul class="space-y-1 opacity-90">
      <li>HPC deployment (CCAST, etc.)</li>
      <li>3D capability</li>
      <li>Multi-GPU scaling tests</li>
    </ul>
  </div>
  <div class="rounded-lg p-4 bg-red-500/10 border border-red-500/30">
    <div class="font-bold text-red-400 mb-2 text-base">Phase 4</div>
    <ul class="space-y-1 opacity-90">
      <li>Immersed Boundary Method</li>
      <li>Dissipative Particle Dynamics</li>
      <li>Full biofluid applications</li>
    </ul>
  </div>
</div>

<div class="mt-6 text-center font-semibold text-primary">
  Flow Solver targeting Exascale Simulations
</div>
