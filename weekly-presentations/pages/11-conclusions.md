---
layout: default
---

# Conclusions

<v-clicks>

- **OvrFlw** is a production-ready AMReX-based incompressible Navier-Stokes solver implementing the IPCS fractional step method on a hybrid staggered/non-staggered grid with MPI + OpenMP + CUDA parallelism.

- **Accuracy validated** against the Taylor–Green vortex and Ghia et al. lid-driven cavity benchmarks ($Re = 100$–$3200$), with results in excellent agreement.

- **2D and 3D support**: OvrFlw automatically adapts to the dimensionality of the physical problem — validated in 3D against Cortes & Miller and Albensoeder et al. (2005) for the lid-driven cavity and reproducing correct vortex breakdown dynamics for the Taylor–Green vortex at $Re = 1600$.

- **Demonstrated exascale scalability**: near-ideal strong scaling (×2,060 on 2,048 CPUs) and efficient weak scaling (32 → 16,384 CPUs, +12% overhead) on ALCF Aurora; comparable weak scaling validated on NERSC Perlmutter. Computational speed is accelerated 20-30 times on multi-GPU architecture.

- **Production-scale 3D simulation** at $Re = 30{,}000$ on a $1024^3$ grid with 16,384 MPI ranks achieves $\sim\!1.9\,\text{s/step}$ on Aurora, confirming readiness for exa-scale incompressible flow simulations.

</v-clicks>

<div class="abs-br m-6 text-sm opacity-50 flex items-start gap-3">
  <span style="white-space:nowrap">Contact OvrFlw Team:</span>
  <div>
    Dr. Trung B. Le &nbsp;·&nbsp; trung.le@ndsu.edu <br>
    Thien-Tam Nguyen &nbsp;·&nbsp; tam.thien.nguyen@ndsu.edu
  </div>
</div>
