---
layout: default
---

# Motivations

<p class="text-sm opacity-60 mt-1 mb-5">Biofluid &amp; biomechanics simulation at physiological scales presents four key challenges:</p>

<div class="grid grid-cols-2 gap-4">
  <div class="border border-primary/30 rounded-lg p-4 bg-primary/5">
    <h3 class="font-bold text-base mb-2">1 · Mathematical Model Fidelity</h3>
    <p class="text-sm opacity-75">Accurate representation of non-Newtonian blood rheology at micro scales, vascular wall elasticity, thrombus formation, and cellular deformation.</p>
  </div>
  <div class="border border-primary/30 rounded-lg p-4 bg-primary/5">
    <h3 class="font-bold text-base mb-2">2 · Multi-scale Interface Coupling</h3>
    <p class="text-sm opacity-75">Robust interface conditions bridging continuum and atomistic simulations. Mass conservation is paramount; momentum and energy conservation are advantageous yet challenging.</p>
  </div>
  <div class="border border-primary/30 rounded-lg p-4 bg-primary/5">
    <h3 class="font-bold text-base mb-2">3 · Non-stationary Data Handling</h3>
    <p class="text-sm opacity-75">Multi-scale simulations require effective averaging and filtering strategies to extract meaningful continuum-scale information from atomistic data.</p>
  </div>
  <div class="border border-primary/30 rounded-lg p-4 bg-primary/5">
    <h3 class="font-bold text-base mb-2">4 · Extreme Computational Demand</h3>
    <p class="text-sm opacity-75">Billions of DOF needed to resolve cell–endothelial interactions within 1 mm³. Local refinement essential for platelet aggregation and thrombus dynamics.</p>
  </div>
</div>

---
layout: default
---

# Goal & Roadmap

<div class="text-sm opacity-75 mt-1 mb-4 grid grid-cols-2 gap-x-8 gap-y-1">
  <div><span class="font-semibold">Solver:</span> Incompressible Navier-Stokes via fractional step (Kim &amp; Moin) on a hybrid staggered/non-staggered grid — contravariant velocities at face centers, Cartesian velocities &amp; pressure at cell centers.</div>
  <div><span class="font-semibold">Numerics:</span> 4-stage RK4 pseudo-time-stepping for momentum; AMReX MLMG (default) or GMRES for the pressure Poisson equation; 2nd-order spatial accuracy.</div>
  <div><span class="font-semibold">Parallelism:</span> MPI + OpenMP + optional CUDA; built on AMReX for block-structured mesh management and GPU portability.</div>
  <div><span class="font-semibold">Validation:</span> Taylor-Green Vortex (exact analytical) and lid-driven cavity vs. Ghia et al. (1982); production 3D run at 1 billion grid resolution, Re = 30,000 on ALCF Aurora and NERCS Perlmutter.</div>
</div>

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
      <li>Adaptive Mesh Refinement</li>
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
