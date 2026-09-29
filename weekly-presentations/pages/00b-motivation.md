---
layout: default
---

# Motivation: Blood Flow Across Scales

<div style="display:grid; grid-template-columns:5fr 6fr; gap:1.5rem; margin-top:0.5rem; align-items:start;">
  <div class="text-center">
    <img :src="'/assets/images/blood-modeling-scales.png'" class="rounded bg-white" style="max-height:330px; width:100%; object-fit:contain" alt="Time and length scales of blood modeling" />
    <div class="text-xs opacity-50 mt-1">Credit: Perdikaris, Grinberg &amp; Karniadakis, <em>Phys. Fluids</em> (2016). DOI: 10.1063/1.4941315</div>
  </div>
  <div>
    <p class="text-sm opacity-70 !mt-0 !mb-3">Simulating whole blood, from vessel networks down to single cells, faces four key challenges:</p>
    <div class="space-y-2 text-sm">
      <div class="border border-primary/30 rounded-lg px-3 py-2 bg-primary/5">
        <span class="font-bold">1 · Model fidelity:</span>&nbsp;
        <span class="opacity-75">non-Newtonian rheology, wall elasticity, thrombus formation, cell deformation</span>
      </div>
      <div class="border border-primary/30 rounded-lg px-3 py-2 bg-primary/5">
        <span class="font-bold">2 · Multi-scale coupling:</span>&nbsp;
        <span class="opacity-75">robust continuum–atomistic interfaces that conserve mass (and ideally momentum and energy)</span>
      </div>
      <div class="border border-primary/30 rounded-lg px-3 py-2 bg-primary/5">
        <span class="font-bold">3 · Non-stationary data:</span>&nbsp;
        <span class="opacity-75">averaging and filtering to extract continuum-scale information from transient, atomistic data</span>
      </div>
      <div class="border border-primary/30 rounded-lg px-3 py-2 bg-primary/5">
        <span class="font-bold">4 · Computational demand:</span>&nbsp;
        <span class="opacity-75">billions of DOF to resolve cell–endothelial interactions within 1 mm³; local refinement is essential</span>
      </div>
    </div>
  </div>
</div>

<div class="mt-4 grid grid-cols-2 gap-4 text-sm">
  <div><span class="font-semibold text-primary">Part 1 · Simulate:</span> <span class="opacity-75">OvrFlw, a verified and validated exascale-ready CFD solver for high-fidelity flow data</span></div>
  <div><span class="font-semibold text-primary">Part 2 · Learn:</span> <span class="opacity-75">unsupervised learning (DMD) on high-fidelity CFD to stratify aneurysm patients</span></div>
</div>
