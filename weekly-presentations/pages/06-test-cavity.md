---
layout: default
---

# Test Case 2: Lid-Driven Cavity

The **lid-driven cavity** is a canonical CFD benchmark: a fluid-filled domain where the top surface translates at constant velocity $U = 1$. All remaining walls impose no-slip conditions. 

For the **3D extension**, the depth $L_y = \Gamma \cdot L_x$ introduces end-wall effects absent in the 2D case and the aspect ratio $\Gamma$ governs the transition between quasi-2D and fully 3D flow regimes.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:2.5rem; margin-top:0.75rem; align-items:center;">

  <div class="text-center">
    <img :src="'/assets/images/cavity-2d-diagram.svg'" style="max-height:280px; width:100%; object-fit:contain" alt="2D cavity diagram" />
  </div>

  <div class="text-center">
    <img :src="'/assets/images/cavity-3d-domain.svg'" style="max-height:280px; width:100%; object-fit:contain" alt="3D cavity domain" />
    <div class="text-xs opacity-70 mt-1">3D &nbsp;&bull;&nbsp; &Gamma; = L<sub>y</sub> / L<sub>x</sub></div>
  </div>

</div>

---
layout: default
---

# Lid-Driven Cavity: $Re = 100$

<div style="margin-top:0.75rem">
  <img :src="'/assets/images/lid2d-ren100.png'" style="width:100%; max-height:400px; object-fit:contain" alt="Velocity profiles Re=100 vs Ghia et al." />
  <div class="text-xs text-center opacity-60 mt-1">Grid 128 &times; 128 &nbsp;&bull;&nbsp; velocity profiles vs. Ghia et al. (1982)</div>
</div>

---
layout: default
---

# Lid-Driven Cavity: $Re = 400$

<div style="margin-top:0.75rem">
  <img :src="'/assets/images/lid2d-ren400.png'" style="width:100%; max-height:400px; object-fit:contain" alt="Velocity profiles Re=400 vs Ghia et al." />
  <div class="text-xs text-center opacity-60 mt-1">Grid 128 &times; 128 &nbsp;&bull;&nbsp; velocity profiles vs. Ghia et al. (1982)</div>
</div>

---
layout: default
---

# Lid-Driven Cavity: $Re = 1000$

<div style="margin-top:0.75rem">
  <img :src="'/assets/images/lid2d-ren1000.png'" style="width:100%; max-height:400px; object-fit:contain" alt="Velocity profiles Re=1000 vs Ghia et al." />
  <div class="text-xs text-center opacity-60 mt-1">Grid 128 &times; 128 &nbsp;&bull;&nbsp; velocity profiles vs. Ghia et al. (1982)</div>
</div>

---
layout: default
---

# Streamlines: Reynolds Number Comparison

<div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:1.25rem; margin-top:0.75rem;">
  <div class="text-center">
    <img :src="'/assets/images/lid2d-streamline-ren100.png'" style="height:220px; width:100%; object-fit:contain" alt="Streamlines Re=100" />
    <div class="text-sm font-semibold mt-1">Re = 100</div>
    <div class="text-xs opacity-50 mb-2">128 &times; 128</div>
    <div class="text-xs opacity-70 text-left">Single dominant vortex; weak secondary eddies confined to bottom corners. Flow is laminar and steady.</div>
  </div>
  <div class="text-center">
    <img :src="'/assets/images/lid2d-streamline-ren400.png'" style="height:220px; width:100%; object-fit:contain" alt="Streamlines Re=400" />
    <div class="text-sm font-semibold mt-1">Re = 400</div>
    <div class="text-xs opacity-50 mb-2">128 &times; 128</div>
    <div class="text-xs opacity-70 text-left">Primary vortex migrates toward center; bottom-right corner eddy intensifies as inertia grows.</div>
  </div>
  <div class="text-center">
    <img :src="'/assets/images/lid2d-streamline-ren3200.png'" style="height:220px; width:100%; object-fit:contain" alt="Streamlines Re=3200" />
    <div class="text-sm font-semibold mt-1">Re = 3,200</div>
    <div class="text-xs opacity-50 mb-2">256 &times; 256</div>
    <div class="text-xs opacity-70 text-left">All three corner vortices well-developed; top-left eddy emerges. Flow approaching transition to unsteadiness.</div>
  </div>
</div>
