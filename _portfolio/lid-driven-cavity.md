---
title: "Lid-Driven Cavity (iFluid)"
excerpt: "The standard benchmark for incompressible flow solvers: a moving lid drives a primary vortex with secondary corner vortices.<br/><img src='/images/cfd/lid-driven-cavity-thumb.png' style='max-width:300px;'>"
collection: portfolio
---

The most widely used **benchmark** for incompressible flow solvers, simulated
with the **iFluid** solver in **FronTier++**.
Fluid sits in a square cavity whose top wall slides at constant velocity, driving
a large primary vortex in the center plus smaller counter-rotating vortices in the
bottom corners. Results are conventionally compared against the Ghia, Ghia & Shin
(1982) reference data.

<figure>
  <a href="/images/cfd/lid-driven-cavity.gif">
    <img src="/images/cfd/lid-driven-cavity.gif" alt="Lid-driven cavity simulation"
         style="max-width:100%;border:1px solid #ddd;border-radius:6px;">
  </a>
  <figcaption>Velocity field / streamlines reaching steady state (no-slip walls, moving lid).</figcaption>
</figure>

See this and other cases on the **[iFluid — CFD Examples](/ifluid/)** page.
