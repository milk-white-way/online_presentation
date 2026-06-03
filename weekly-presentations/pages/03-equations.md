---
layout: default
---

# Governing Equations

The **incompressible Navier–Stokes equations** form the basis of the solver:

$$\nabla \cdot \mathbf{u} = 0$$

$$\rho \left( \frac{\partial \mathbf{u}}{\partial t} + \mathbf{u} \cdot \nabla \mathbf{u} \right) = -\nabla p + \mu \, \nabla^2 \mathbf{u}$$

For large-scale applications, solving the coupled system demands excessive memory and poor iterative efficiency. Instead we use a **segregated (projection) method** — the **Incremental Pressure Correction Scheme (IPCS)** — splitting velocity and pressure into sequential solves.

---
layout: default
---

# IPCS: Fractional Step Method

**Step 1 — Tentative velocity** (ignore pressure increment)

$$\rho \frac{\mathbf{u}^* - \mathbf{u}^n}{\Delta t} + \rho \left( \mathbf{u}^n \cdot \nabla \right) \mathbf{u}^n = -\nabla p^n + \mu \, \nabla^2 \mathbf{u}^*$$

**Step 2 — Pressure correction** (enforce divergence-free constraint)

$$\nabla^2 p^{n+1} = \nabla^2 p^n - \frac{\rho}{\Delta t} \nabla \cdot \mathbf{u}^*$$

**Step 3 — Velocity correction**

$$\mathbf{u}^{n+1} = \mathbf{u}^* - \frac{\Delta t}{\rho} \nabla \left( p^{n+1} - p^n \right)$$
