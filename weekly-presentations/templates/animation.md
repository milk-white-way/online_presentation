---
layout: default
---

# Animation Title

Brief context or caption for the animation.

<!-- ============================================================
     OPTION A — WebM / MP4 video (recommended for CFD simulations)
     Best for: velocity fields, vorticity contours, particle traces
     - Use WebM for smallest file size
     - autoplay loop muted playsinline are all required for browser autoplay
     - Place files in public/assets/figures/
     ============================================================ -->

<div class="flex justify-center mt-4">
  <video
    :src="'/assets/figures/animation.webm'"
    autoplay loop muted playsinline
    class="rounded-lg max-h-80"
  />
</div>

<!-- ============================================================
     OPTION B — Side-by-side: parameters left, video right
     ============================================================

---
layout: two-cols
---

# Animation Title

**Parameters:**
- Grid: $256 \times 256$
- Re = 3200
- $t^* = 0$ to $160$

::right::

<div class="flex items-center justify-center h-full">
  <video
    :src="'/assets/figures/animation.webm'"
    autoplay loop muted playsinline
    class="rounded-lg w-full"
  />
</div>

============================================================ -->

<!-- ============================================================
     OPTION C — Animated WebP / GIF (simple diagrams, schematics)
     Works in <img> tag — no video element needed
     ============================================================

<div class="flex justify-center mt-4">
  <img :src="'/assets/figures/animation.webp'" class="rounded-lg max-h-80" alt="Animation" />
</div>

============================================================ -->
