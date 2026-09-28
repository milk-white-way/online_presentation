---
layout: two-cols
---

# Numerical Method

<div class="text-sm">

Incompressible Navier–Stokes (dimensionless):

$$
\frac{\partial \mathbf{V}}{\partial t} + (\mathbf{V} \cdot \nabla)\mathbf{V} + \nabla p - \text{Re}^{-1} \nabla^2 \mathbf{V} = 0, \qquad \nabla \cdot \mathbf{V} = 0
$$

**Fractional step:** Incremental Pressure Correction Scheme (IPCS), BDF2 in time:

$$
\begin{align*}
  \text{I}   &: \tfrac{1}{2\Delta t}\left(3V^{*} - 4V^n + V^{n-1}\right) + \nabla p^n + \left[C_h - \text{Re}^{-1}\nabla_h^2\right]V^{*} = 0 \\[4pt]
  \text{II}  &: \tfrac{3}{2\Delta t}\left(\mathbf{V}^{n+1} - \mathbf{V}^{*}\right) = -\nabla\phi^{n+1}, \quad \nabla \cdot \mathbf{V}^{n+1} = 0 \\[4pt]
  \text{III} &: p^{n+1} = p^{n} + \phi^{n+1}
\end{align*}
$$

<div class="mt-4 rounded-lg px-3 py-2 border border-primary/30 text-xs">
  <div class="flex items-center gap-3 mb-1">
    <span class="rounded bg-white px-1.5 py-1 inline-flex"><img :src="'/assets/images/AMReX.png'" style="height:18px" alt="AMReX" /></span>
    <span class="text-sm font-semibold whitespace-nowrap">Built on AMReX</span>
    <span class="opacity-60 whitespace-nowrap">LBNL · Exascale Computing Project</span>
  </div>
  <div class="opacity-80 leading-relaxed">Block-structured adaptive mesh refinement · cell- and face-centered data · portable and scalable on CPUs and GPUs · interfaces to HYPRE and PETSc · output for yt, Amrvis, ParaView, VisIt</div>
  <div class="opacity-50 mt-1">W. Zhang et al., <em>J. Open Source Softw.</em> 4(37):1370, 2019</div>
</div>

</div>

::right::

<div class="flex flex-col items-center h-full pt-4 pl-4">
  <img :src="'/assets/images/hybrid-grid.png'" class="rounded" style="max-height:260px; max-width:100%; object-fit:contain" alt="Hybrid staggered/non-staggered grid" />
  <ul class="text-sm mt-3 space-y-1">
    <li><strong>Hybrid grid:</strong> velocities at cell faces (staggered), pressure at cell centers</li>
    <li><strong>Momentum (I):</strong> RK4 pseudo-time iterations</li>
    <li><strong>Poisson (II):</strong> AMReX MLMG (default) or GMRES</li>
    <li>2nd-order in space · MPI + OpenMP + CUDA via AMReX</li>
  </ul>
</div>
