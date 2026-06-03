---
layout: default
---

# Figure Grid Title

Shared context: Grid $256 \times 256$, $t^* = 160$

<div class="grid grid-cols-3 gap-4 mt-4">
  <div class="text-center">
    <img :src="'/assets/backgrounds/bg1.jpg'" class="rounded w-full object-cover opacity-70" style="height:180px" alt="Case 1" />
    <!-- replace /assets/backgrounds/bg1.jpg -->
    <p class="mt-2 text-sm font-semibold">Label 1</p>
  </div>
  <div class="text-center">
    <img :src="'/assets/backgrounds/bg2.jpg'" class="rounded w-full object-cover opacity-70" style="height:180px" alt="Case 2" />
    <!-- replace /assets/backgrounds/bg2.jpg -->
    <p class="mt-2 text-sm font-semibold">Label 2</p>
  </div>
  <div class="text-center">
    <img :src="'/assets/backgrounds/bg3.jpg'" class="rounded w-full object-cover opacity-70" style="height:180px" alt="Case 3" />
    <!-- replace /assets/backgrounds/bg3.jpg -->
    <p class="mt-2 text-sm font-semibold">Label 3</p>
  </div>
</div>
