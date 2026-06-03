---
layout: two-cols
---

# Test Case 2: Lid-Driven Cavity

**Setup:**
- Square domain, $L = 1$
- Top lid moves at constant velocity $U = 1$
- All other walls: no-slip ($\mathbf{u} = 0$)
- Reynolds numbers tested: $Re = 100,\, 400,\, 3200,\, 10000$

$$Re = \frac{U L}{\nu}$$

::right::

<div class="flex items-center justify-center h-full">
  <div style="display:grid;grid-template-columns:42px 148px 42px;grid-template-rows:44px 148px 36px;font-size:11px;text-align:center">
    <div></div>
    <div style="display:flex;align-items:flex-end;justify-content:center;padding-bottom:5px;color:#4EC5D4;font-weight:600">Moving Lid &nbsp; U = 1 →</div>
    <div></div>
    <div style="display:flex;align-items:center;justify-content:center;writing-mode:vertical-rl;transform:rotate(180deg);opacity:0.75">No-slip</div>
    <div style="border:2px solid rgba(255,255,255,0.7);position:relative">
      <div style="position:absolute;top:0;left:0;right:0;height:3px;background:#4EC5D4"></div>
      <div style="position:absolute;top:0;left:0;right:0;bottom:0;display:flex;align-items:center;justify-content:center;opacity:0.3;font-size:14px">L = 1</div>
    </div>
    <div style="display:flex;align-items:center;justify-content:center;writing-mode:vertical-rl;opacity:0.75">No-slip</div>
    <div></div>
    <div style="display:flex;align-items:flex-start;justify-content:center;padding-top:5px;opacity:0.75">No-slip</div>
    <div></div>
  </div>
</div>

---
layout: image-right
image: /assets/backgrounds/bg1.jpg
---

# Lid-Driven Cavity: $Re = 100$

<!-- replace /assets/backgrounds/bg1.jpg with streamlines/velocity contour at Re=100 -->

- Grid: $128 \times 128$
- Reynolds number: $Re = 100$
- Single primary vortex centered in the cavity
- Results agree with Ghia et al. (1982) benchmark

---
layout: image-right
image: /assets/backgrounds/bg2.jpg
---

# Lid-Driven Cavity: $Re = 400$

<!-- replace /assets/backgrounds/bg2.jpg with streamlines/velocity contour at Re=400 -->

- Grid: $128 \times 128$
- Reynolds number: $Re = 400$
- Primary vortex shifts toward cavity center
- Secondary corner vortices begin to develop

---
layout: image-right
image: /assets/backgrounds/bg3.jpg
---

# Lid-Driven Cavity: $Re = 3200$

<!-- replace /assets/backgrounds/bg3.jpg with streamlines/velocity contour at Re=3200 -->

- Grid: $256 \times 256$
- Reynolds number: $Re = 3200$
- Non-dimensional time: $t^* = 160$
- Strong secondary vortices in bottom corners
- Flow exhibits unsteady behavior

---
layout: image-right
image: /assets/backgrounds/bg1.jpg
---

# Lid-Driven Cavity: $Re = 10000$

<!-- replace /assets/backgrounds/bg1.jpg with streamlines/velocity contour at Re=10000 -->

- Grid: $256 \times 256$
- Reynolds number: $Re = 10000$
- Non-dimensional time: $t^* = 160$
- Highly unsteady, complex vortex structures throughout the cavity

---
layout: default
---

# Streamlines: All Reynolds Numbers

**Grid:** $256 \times 256$

<div class="grid grid-cols-3 gap-4 mt-4">
  <div class="text-center">
    <!-- replace with Re=400 streamline plot -->
    <img :src="'/assets/backgrounds/bg1.jpg'" class="rounded-lg w-full h-44 object-cover opacity-70" alt="Re=400 placeholder" />
    <p class="mt-2 text-sm font-semibold">Re = 400</p>
  </div>
  <div class="text-center">
    <!-- replace with Re=3200 streamline plot -->
    <img :src="'/assets/backgrounds/bg2.jpg'" class="rounded-lg w-full h-44 object-cover opacity-70" alt="Re=3200 placeholder" />
    <p class="mt-2 text-sm font-semibold">Re = 3,200</p>
  </div>
  <div class="text-center">
    <!-- replace with Re=10000 streamline plot -->
    <img :src="'/assets/backgrounds/bg3.jpg'" class="rounded-lg w-full h-44 object-cover opacity-70" alt="Re=10000 placeholder" />
    <p class="mt-2 text-sm font-semibold">Re = 10,000</p>
  </div>
</div>
