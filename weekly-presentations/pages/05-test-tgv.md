---
layout: two-cols
---

# Test Case 1: Taylor–Green Vortex

**Analytical solution** (2D, periodic domain):

$$u = -\cos(x)\sin(y)\,e^{-2\nu t}$$

$$v = \;\;\sin(x)\cos(y)\,e^{-2\nu t}$$

$$p = -\tfrac{1}{4}\left[\cos(2x) + \cos(2y)\right]e^{-4\nu t}$$

**Parameters:**
- Domain: $[0, 2\pi]^2$, periodic BC
- Grid: $128 \times 128$
- $t = 0.1\,\text{s}$, $\;\Delta t = 2 \times 10^{-6}$

::right::

<div class="flex items-center justify-center h-full">
  <img :src="'/assets/images/tgv2d.png'" class="rounded" style="max-height:440px; max-width:100%; object-fit:contain" alt="TGV velocity field 128×128" />
</div>

---
layout: two-cols
---

# Taylor–Green Vortex: 3D Simulation

**Domain:** $\Omega = [-\pi,\pi]^3$, periodic BC &nbsp;·&nbsp; $Re = 1600$

Initial conditions at $t = 0$:

$$u_x = \sin(x)\cos(y)\cos(z)$$

$$u_y = -\cos(x)\sin(y)\cos(z)$$

$$u_z = 0$$

$$p = \tfrac{1}{16}\bigl[\cos(2x)+\cos(2y)\bigr]\bigl[\cos(2z)+2\bigr]$$

The 3D TGV is the canonical benchmark for turbulence onset: the initially laminar vortex sheet undergoes vortex stretching and cascades energy to small scales.

::right::

<div class="flex flex-col items-center justify-center h-full gap-2">
  <video :src="'/assets/media/isoView-velocityContours-3Dtgv.webm'" autoplay loop muted playsinline class="rounded" style="max-height:420px; max-width:100%; object-fit:contain"></video>
  <div class="text-xs text-center opacity-60">Velocity iso-contours during vortex breakdown</div>
</div>
