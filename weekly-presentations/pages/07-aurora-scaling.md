---
layout: default
---

# Scaling Benchmark on AURORA

**OvrFlw** · 3D lid-driven cavity · ALCF Aurora HPC

<div style="display:grid; grid-template-columns:1fr 1fr; gap:0 1.5rem; margin-top:0.5rem;">
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 6px">Strong Scaling</div>
    <img :src="'/assets/images/aurora-strong.png'" class="w-full rounded" style="max-height:320px; object-fit:contain" alt="Strong scaling" />
    <div class="text-xs opacity-50" style="margin:5px 0 0">
      1 → 2,048 CPUs · speedup ×2,060 · tracks ideal up to 2,048 CPUs
    </div>
  </div>
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 6px">Weak Scaling</div>
    <img :src="'/assets/images/aurora-weak.png'" class="w-full rounded" style="max-height:320px; object-fit:contain" alt="Weak scaling" />
    <div class="text-xs opacity-50" style="margin:5px 0 0">
      32 → 16,384 CPUs · time/step +12% across 512× resource growth
    </div>
  </div>
</div>

---
layout: default
---

# Scaling on Perlmutter

<div style="display:grid; grid-template-columns:1fr 1fr; gap:1.5rem; margin-top:0.5rem;">
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 6px">Weak Scaling — Perlmutter</div>
    <img :src="'/assets/images/perlmutter-weak.png'" style="height:300px; width:100%; object-fit:contain" alt="Weak scaling Perlmutter" />
    <div class="text-xs opacity-60 mt-2 text-left">Weak scaling on NERSC Perlmutter: problem size grows proportionally with core count. Near-constant time-per-step confirms efficient parallel decomposition across NVIDIA A100 nodes. GPU acceleration was 20-30 folds faster in computation compared to CPU.</div>
  </div>
  <div class="text-center">
    <div class="text-sm font-semibold opacity-70" style="margin:0 0 6px">Aurora vs. Perlmutter CPU</div>
    <img :src="'/assets/images/aurora-vs-perlmutter-cpu.png'" style="height:300px; width:100%; object-fit:contain" alt="Aurora vs Perlmutter CPU comparison" />
    <div class="text-xs opacity-60 mt-2 text-left">Head-to-head comparison at matched problem sizes. Aurora GPU nodes deliver substantially higher throughput than Perlmutter CPU nodes, most prominent from 256 to 2048 CPUs. This result potentially show the performance difference between two MPI implementations based on their corresponding hardware architectures (Intel vs AMD). </div>
  </div>
</div>
