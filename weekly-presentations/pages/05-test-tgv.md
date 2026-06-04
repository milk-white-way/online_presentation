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
layout: default
---

# Taylor–Green Vortex: 3D Simulation

<div class="flex flex-col items-center justify-center h-4/5 gap-4 opacity-50">
  <div class="border-2 border-dashed border-current rounded-xl px-16 py-10 text-center">
    <p class="text-xl font-semibold mb-2">3D velocity iso-contours animation</p>
    <p class="text-sm"> coming soon</p>
  </div>
</div>
