---
layout: default
---

# Governing Equations

Incompressible Navier-Stokes in dimensionless form:

$$
\begin{align*}
  \frac{\partial \mathbf{V}}{\partial t} + \text{C}(\mathbf{V}) &+ \nabla p - \text{Re}^{-1} \nabla^2 \mathbf{V} = 0 \\[2pt]
  \nabla \cdot \mathbf{V} &= 0
\end{align*}
$$

where $\text{C}(\mathbf{V}) = (\mathbf{V} \cdot \nabla)\mathbf{V}$ is the convective operator, $\text{Re} = UL/\nu$ is the Reynolds number.

The set of equations is solved via **Fractional Step Method**. We employ the projection method that called Incremental Pressure Correction Scheme (IPCS) such that:

$$
\begin{align*}
  \text{I}   &: \frac{1}{2\Delta t}\left(3V^{*} - 4V^n + V^{n-1}\right) + \nabla p^n + \left[C_h - \text{Re}^{-1}\nabla_h^2\right]V^{*} \\[6pt]
  \text{II}  &: \begin{cases}
                  \dfrac{3}{2\Delta t}\left(\mathbf{V}^{n+1} - \mathbf{V}^{*}\right) = -\nabla\phi^{n+1} \\[4pt]
                  \nabla \cdot \mathbf{V}^{n+1} = 0
                \end{cases} \\[12pt]
  \text{III} &: p^{n+1} = p^{k} + \phi^{n+1}
\end{align*}
$$
