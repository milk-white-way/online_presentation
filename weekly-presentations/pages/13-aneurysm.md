---
layout: default
class: p-0
hide: true
---

<div class="absolute inset-0 bg-black"></div>

<SlidevVideo autoplay autoreset="slide" print-timestamp="15" class="absolute inset-0 w-full h-full object-contain">
  <source :src="'/assets/media/aneurysm-motivation.webm'" type="video/webm" />
</SlidevVideo>

<div class="absolute top-6 left-10 text-xs tracking-widest uppercase text-white opacity-60">
  Hemodynamics of Brain Aneurysms
</div>

---
layout: default
---

# Patient-specific Cohort &amp; Modal Analysis

<div style="display:grid; grid-template-columns:auto auto 1fr; gap:1.25rem; margin-top:0.5rem; align-items:start;">
  <div class="text-center">
    <img :src="'/assets/images/aneurysm/fig1.png'" style="height:315px; object-fit:contain" alt="Six patient-specific ICA aneurysms grouped by size" />
    <div class="text-xs opacity-60 mt-1">6 ICA aneurysms (AneuRisk), clustered by size</div>
  </div>
  <div class="text-center">
    <img :src="'/assets/images/aneurysm/fig2.png'" style="height:315px; object-fit:contain" alt="Modeling, CFD, and DMD pipeline" />
    <div class="text-xs opacity-60 mt-1">Modeling → CFD → modal analysis</div>
  </div>
  <div class="text-xs leading-relaxed space-y-3 pt-2">
    <div>
      <div class="font-semibold text-sm">CFD (in-house CURVIB)</div>
      <div class="opacity-75">201 × 201 × 321 grid (≈ 12 M points), 0.07–0.15 mm in the sac</div>
    </div>
    <div>
      <div class="font-semibold text-sm">Pulsatile inflow</div>
      <div class="opacity-75">72 bpm waveform with harmonics at 1.2, 2.4, 3.6 Hz; <em>Re</em> ≈ 550, <em>α</em> ≈ 3; 4 cycles × 4,000 steps</div>
    </div>
    <div>
      <div class="font-semibold text-sm">Question</div>
      <div class="opacity-75">Can modal analysis characterize aneurysmal flow from data at <em>clinical</em> resolution (≈ 1 mm, ≈ 40 ms)?</div>
    </div>
  </div>
</div>

<div class="mt-3 rounded-lg px-3 py-2 text-xs border border-primary/30">
  <span class="font-semibold text-sm">Hankel DMD</span>&nbsp; decomposes the sac flow into 3D spatial modes, frequency pseudo-spectra, and cumulative-energy (CE) curves ·
  <span class="font-semibold">72 datasets</span> = 6 patients × 4 spatial (0.12 → ≈ 1 mm) × 3 temporal (Δτ = 16.8 → 4.2 ms) resolutions
</div>

---
layout: default
hide: true
---

# Modal Analysis via Hankel DMD

Stack $M+1$ velocity snapshots in the aneurysm sac, add a time-delay (Hankel) embedding, and fit a best linear operator:

$$
\mathbf{X}_{H} = \begin{bmatrix} \mathbf{V}_0 & \mathbf{V}_1 & \cdots & \mathbf{V}_{M-1} \\ \mathbf{V}_1 & \mathbf{V}_2 & \cdots & \mathbf{V}_{M} \end{bmatrix},
\qquad \mathbf{Y} \approx \mathbf{A}\mathbf{X}_H,
\qquad \mathbf{A}\boldsymbol{\varphi}_k = \lambda_k \boldsymbol{\varphi}_k
$$

<div class="grid grid-cols-3 gap-4 mt-4 text-sm">
  <div class="border border-primary/30 rounded-lg p-3 bg-primary/5">
    <div class="font-bold mb-1">Spatial modes <em>φ<sub>k</sub></em></div>
    <div class="opacity-75 text-xs">3D coherent structures, each oscillating at a single frequency <em>f<sub>k</sub></em> from <em>λ<sub>k</sub></em></div>
  </div>
  <div class="border border-primary/30 rounded-lg p-3 bg-primary/5">
    <div class="font-bold mb-1">Pseudo-spectrum</div>
    <div class="opacity-75 text-xs">Temporal magnitude |<em>b<sub>k</sub> λ<sub>k</sub><sup>M</sup></em>| vs. <em>f<sub>k</sub></em>: which frequencies persist over the cardiac cycle</div>
  </div>
  <div class="border border-primary/30 rounded-lg p-3 bg-primary/5">
    <div class="font-bold mb-1">Cumulative energy (CE)</div>
    <div class="opacity-75 text-xs">From the singular values of <strong>X</strong><sub>H</sub>: how fast the flow energy is captured by the leading modes</div>
  </div>
</div>

<div class="mt-4 text-sm">
  <span class="font-semibold">72 datasets</span>&nbsp;
  <span class="opacity-75">= 6 patients × 4 spatial resolutions (1X–8X, 0.12 → ≈ 1 mm) × 3 temporal resolutions (<em>M</em> = 50, 100, 200; Δτ = 16.8 → 4.2 ms)</span>
</div>

<div class="abs-bl m-4 text-xs opacity-50">
  Hankel DMD: Kamb et al. (2020); Optimized DMD: Askham &amp; Kutz, <em>SIAM J. Appl. Dyn. Syst.</em> 17(1), 2018
</div>

---
layout: default
---

# Inflow Jet &amp; Dominant Modes

<div style="display:grid; grid-template-columns:1fr 1fr; gap:1.5rem; margin-top:0.25rem;">
  <div class="text-center">
    <img :src="'/assets/images/aneurysm/fig4.png'" style="height:290px; width:100%; object-fit:contain" alt="Streamlines at peak systole" />
    <div class="text-xs opacity-60 mt-1">Streamlines at peak systole, aligned on the aneurysm axis</div>
  </div>
  <div class="text-center">
    <img :src="'/assets/images/aneurysm/fig5.png'" style="height:290px; width:100%; object-fit:contain" alt="Three most energetic Hankel DMD modes" />
    <div class="text-xs opacity-60 mt-1">Three most energetic Hankel DMD modes (iso-surface |<strong>V</strong>| / |<strong>V</strong>|<sub>max</sub> = 0.5)</div>
  </div>
</div>

<v-clicks>

- The dominant modes recover the **inflow waveform harmonics** (1.2, 2.4, 3.6 Hz) and trace the inflow jet
- Jet type (diffused vs. concentrated), impingement site, and vortex rotation follow the **inflow angle**, not aneurysm size

</v-clicks>

---
layout: default
---

# High-Frequency Fluctuations

<div style="display:grid; grid-template-columns:3fr 2fr; gap:1.5rem; margin-top:0.5rem; align-items:center;">
  <div class="text-center">
    <img :src="'/assets/images/aneurysm/fig7.png'" style="max-height:380px; width:100%; object-fit:contain" alt="Pseudo-spectra and high-frequency modes of Patients 2 and 6" />
    <div class="text-xs opacity-60 mt-1">Patients 2 (small) and 6 (large): pseudo-spectra and modes at the peak frequencies</div>
  </div>
  <div class="text-sm">

<v-clicks>

- Strong, persistent modes far above the inflow harmonics: **50.9 Hz** (P2) and **76.9 Hz** (P6), up to 96% of the dominant mode
- They sit where the jet **impinges on the wall** and the main **vortex forms**
- They appear in both small and large aneurysms, so **size does not predict them**
- At $M = 50$ ($\Delta\tau$ = 16.8 ms) the band stops at 30 Hz and these modes are invisible

</v-clicks>

  </div>
</div>

---
layout: default
---

# Stratification &amp; Robustness

<div style="display:grid; grid-template-columns:1fr 1fr; gap:1.5rem; margin-top:0.25rem;">
  <div>
    <img :src="'/assets/images/aneurysm/fig8.png'" style="height:270px; width:100%; object-fit:contain" alt="Cumulative energy curves at M = 50, 100, 200" />
    <div class="grid grid-cols-2 gap-2 mt-2 text-xs">
      <div class="rounded p-2 bg-sky-500/10 border border-sky-500/30">
        <div class="font-semibold text-sky-500">Laminarized flows</div>
        <div class="opacity-75">P1, P3 · slope ≈ 0.26</div>
      </div>
      <div class="rounded p-2 bg-red-500/10 border border-red-500/30">
        <div class="font-semibold text-red-500">Transient dynamics</div>
        <div class="opacity-75">P2, P4, P5, P6 · slope ≈ 0.20</div>
      </div>
    </div>
    <div class="text-xs opacity-70 mt-2">≈ 10% energy gap at 20% of the modes, consistent for every temporal resolution <em>M</em></div>
  </div>
  <div>
    <img :src="'/assets/images/aneurysm/fig9.png'" style="height:270px; width:100%; object-fit:contain" alt="CE curves across spatial resolutions for Patients 1 and 6" />
    <div class="rounded p-2 mt-2 text-xs bg-green-500/10 border border-green-500/30">
      <div class="font-semibold text-green-500">Robust to coarsening</div>
      <div class="opacity-75">CE curves differ by &lt; 1.5% from CFD resolution (1X) down to 16X, i.e., coarser than 1 mm, comparable to 4D-flow MRI</div>
    </div>
  </div>
</div>

---
layout: default
---

# Takeaways: Aneurysm Hemodynamics

<v-clicks>

- **Patient-specific flow:** DMD reveals unique 3D flow structures in each patient, independent of aneurysm size or aspect ratio.
- **Robust at low resolution:** pseudo-spectra and CE curves characterize the flow even at clinical spatial and temporal resolutions.
- **Toward risk assessment:** the CE slope stratifies patients into *laminarized* vs. *transient* flows, a new quantitative marker for aneurysm severity.

</v-clicks>

<div v-click class="mt-8 rounded-lg p-4 bg-primary/5 border border-primary/30 text-sm">
  <span class="font-semibold">The computational bottleneck:</span>&nbsp;
  <span class="opacity-80">every patient needs ≈ 12 M grid points × 16,000 time steps. Scaling to large cohorts and down to cellular scales requires an exascale-ready flow solver such as OvrFlw.</span>
</div>

<div class="abs-bl m-4 text-xs opacity-50 leading-relaxed">
  T.-T. Nguyen, D. Kasperski, P. K. Huynh, T. Q. Le, T. B. Le, "Modal analysis of blood flows in saccular aneurysms",<br/>
  <em>Phys. Fluids</em> 37, 011906 (2025). DOI: 10.1063/5.0243383
</div>
