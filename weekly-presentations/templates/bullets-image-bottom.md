---
layout: default
---

# Slide Title

Short intro sentence or context.

<v-clicks>

- First point
- Second point
- Third point
- Fourth point

</v-clicks>

<!-- ============================================================
     Wide / banner image anchored below the text.
     Best for: horizontal logos, wide diagrams, panoramic figures.
     - w-full    — spans full slide width
     - object-contain — never crops; shows the full image
     - max-h-36  — limits height so bullets above stay visible
                   adjust to max-h-32 (shorter) or max-h-40 (taller)
     ============================================================ -->
<div class="mt-6">
  <img
    :src="'/assets/figures/wide-figure.png'"
    class="w-full max-h-36 object-contain rounded"
    alt="Figure"
  />
  <!-- replace /assets/figures/wide-figure.png -->
  <p class="text-xs text-center opacity-50 mt-1">Optional caption</p>
</div>
