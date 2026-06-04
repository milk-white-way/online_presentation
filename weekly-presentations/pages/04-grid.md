---
layout: two-cols
---

# Hybrid Staggered / Non-Staggered Grid

<v-clicks>

- Velocity components defined at **cell faces** (staggered)
- Pressure defined at **cell centers** (non-staggered)
- Combines stability advantages of staggered grids with the flexibility of collocated layouts
- **Prescribed boundary conditions** applied at domain boundaries
- **Linear interpolation** used to map values to physical boundary locations

</v-clicks>

::right::

<div class="flex items-center justify-center h-full">
  <img :src="'/assets/images/hybrid-grid.png'" class="rounded" style="max-height:440px; max-width:100%; object-fit:contain" alt="Hybrid staggered/non-staggered grid" />
</div>
