---
layout: two-cols
---

# Test Case 1: Taylor–Green Vortex

**Analytical solution** (2D, periodic domain):

$$u(x, y, t) = -\cos(x)\sin(y)\,e^{-2\nu t}$$

$$v(x, y, t) = \sin(x)\cos(y)\,e^{-2\nu t}$$

$$p(x, y, t) = -\frac{1}{4}\left[\cos(2x) + \cos(2y)\right]e^{-4\nu t}$$

**Parameters:**
- Domain: $[0, 2\pi] \times [0, 2\pi]$, periodic BC
- Grid: $16 \times 16$ → $128 \times 128$
- $\Delta t = 2 \times 10^{-6}$, total steps: 100

::right::

<div class="flex items-center justify-center h-full">
  <!-- replace with actual velocity field plot -->
  <img :src="'/assets/backgrounds/bg1.jpg'" class="rounded-lg opacity-70 max-h-64 object-cover" alt="Velocity field placeholder" />
</div>

---
layout: image-right
image: /assets/backgrounds/bg2.jpg
---

# Taylor–Green Vortex: Results

<!-- replace /assets/backgrounds/bg2.jpg with actual velocity contour plots -->

**Grid:** $16 \times 16$

- Non-dimensional time step: $\Delta t = 2 \times 10^{-6}$
- Total steps: 100
- Solver matches analytical solution with high accuracy

<v-click>

**Grid:** $128 \times 128$

- Simulation time: $t = 0.1\,\text{s}$
- $L^2$ error converges at expected second-order rate

</v-click>
