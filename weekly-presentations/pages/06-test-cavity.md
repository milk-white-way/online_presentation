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

---
layout: default
---

# 3D Lid-Driven Cavity: $\Gamma = 2$, $Re = 100$

<div style="position:relative; width:min(100%,500px); margin:0.4rem auto 0; aspect-ratio:2292/1312;">
  <img :src="'/assets/images/ratio2-1_ren100.png'" style="width:100%; height:100%; object-fit:fill;" alt="3D cavity Re=100 Gamma=2" />
  <div style="position:absolute;left:13%;top:5%;transform:translate(-50%,-50%);background:#f97316;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">①</div>
  <div style="position:absolute;left:37%;top:85%;transform:translate(-50%,-50%);background:#ef4444;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">②</div>
  <div style="position:absolute;left:67%;top:57%;transform:translate(-50%,-50%);background:#16a34a;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">③</div>
</div>
<div class="text-xs text-center opacity-60 mt-1">Aspect ratio &Gamma; = 2 &nbsp;&bull;&nbsp; Re = 100 &nbsp;&bull;&nbsp; steady state (t = 10) &nbsp;&bull;&nbsp; vs. Cortes &amp; Miller and Albensoeder et al. (2005)</div>
<ul class="text-xs mt-2" style="list-style:none; padding:0; line-height:1.65; display:flex; flex-direction:column; gap:0.2rem;">
  <li><span v-mark="{at:0,type:'circle',color:'#f97316'}">① End-wall peak: <em>u</em>&thinsp;≈&thinsp;0.9 at <em>y</em>&thinsp;=&thinsp;&minus;1</span> ==> imprinted by the lateral no-slip boundary.</li>
  <li><span v-mark="{at:0,type:'underline',color:'#ef4444'}">② Velocity dips to &asymp;&thinsp;&minus;0.2 near <em>y</em>&thinsp;=&thinsp;&minus;0.45</span>, then recovers to zero ==> hallmark of end-wall confinement in a finite-span cavity.</li>
  <li><span v-mark="{at:0,type:'highlight',color:'rgba(34,197,94,0.35)'}">③ OvrFlw is in excellent agreement with both Cortes &amp; Miller and Albensoeder et al. (2005) across the full span.</span></li>
</ul>

---
layout: default
---

# 3D Lid-Driven Cavity: $\Gamma = 2$, $Re = 1000$

<div style="position:relative; width:min(100%,500px); margin:0.4rem auto 0; aspect-ratio:2292/1312;">
  <img :src="'/assets/images/ratio2-1_ren1000.png'" style="width:100%; height:100%; object-fit:fill;" alt="3D cavity Re=1000 Gamma=2" />
  <div style="position:absolute;left:14%;top:6%;transform:translate(-50%,-50%);background:#f97316;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">①</div>
  <div style="position:absolute;left:38%;top:55%;transform:translate(-50%,-50%);background:#ef4444;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">②</div>
  <div style="position:absolute;left:59%;top:87%;transform:translate(-50%,-50%);background:#0891b2;color:white;border-radius:50%;width:20px;height:20px;font-size:11px;font-weight:700;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 5px rgba(0,0,0,.55);z-index:2">③</div>
</div>
<div class="text-xs text-center opacity-60 mt-1">Aspect ratio &Gamma; = 2 &nbsp;&bull;&nbsp; Re = 1,000 &nbsp;&bull;&nbsp; t = 200 &nbsp;&bull;&nbsp; vs. Cortes &amp; Miller and Albensoeder et al. (2005)</div>
<ul class="text-xs mt-2" style="list-style:none; padding:0; line-height:1.65; display:flex; flex-direction:column; gap:0.2rem;">
  <li><span v-mark="{at:0,type:'box',color:'#f97316'}">① Near-wall peak: <em>u</em>&thinsp;≈&thinsp;0.88 at <em>y</em>&thinsp;=&thinsp;&minus;1</span> ==> end-wall imprint persists despite strong inertia.</li>
  <li>② First zero-crossing near <em>y</em>&thinsp;≈&thinsp;&minus;0.5 ==> onset of inertia-driven spanwise variability as end-wall layers interact with the vortex core.</li>
  <li><span v-mark="{at:0,type:'highlight',color:'rgba(8,145,178,0.3)'}">③ Pronounced minimum <em>u</em>&thinsp;≈&thinsp;&minus;0.3 near mid-span (<em>y</em>&thinsp;≈&thinsp;0)</span> ==> deepened return flow driven by the primary cavity vortex.</li>
</ul>
