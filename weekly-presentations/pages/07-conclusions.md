---
layout: default
---

# Conclusions

<v-clicks>

- The **2D solver achieves high accuracy**, validated against both the Taylor–Green vortex exact solution and the Ghia et al. lid-driven cavity benchmark across a wide range of Reynolds numbers ($Re = 100$ to $10000$).

- **Fixed Point Iteration** and **Newton–Krylov** methods are implemented, giving the solver flexibility to handle both weakly and strongly nonlinear flow regimes.

- The application can be **deployed on HPC clusters**, demonstrating its readiness for large-scale scientific computing workflows.

</v-clicks>

---
layout: default
---

# Future Works

<v-clicks>

- **3D capability** — extend the solver to three-dimensional problems, enabling simulation of realistic biofluid and engineering flow configurations.

- **Adaptive Mesh Refinement (AMR)** — leverage AMReX's native AMR support to concentrate resolution only where needed, significantly reducing computational cost.

- **Multi-GPU scaling** — implement and validate multi-GPU code paths to fully exploit modern exascale architectures (e.g., FRONTIER, AURORA).

</v-clicks>

<div class="abs-br m-6 text-sm opacity-50">
  Thien-Tam Nguyen · tam.thien.nguyen@ndsu.edu
</div>
