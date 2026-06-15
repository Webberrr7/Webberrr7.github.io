---
title: "Taylor–Green Vortex (iFluid)"
excerpt: "Accuracy-verification case for the incompressible Navier–Stokes solver, with a known analytical solution.<br/><img src='/images/cfd/taylor-green-thumb.png' style='max-width:300px;'>"
collection: portfolio
---

A classic **accuracy-verification** problem simulated with the **iFluid** solver
in **FronTier++**. An array of
counter-rotating vortices decays in time under viscosity; because the 2-D
incompressible Navier–Stokes equations have an *exact analytical solution* for
this flow, it is the standard test for confirming a solver reproduces the correct
decay rate and vortex structure.

<figure>
  <a href="/images/cfd/taylor-green.gif">
    <img src="/images/cfd/taylor-green.gif" alt="Taylor–Green vortex simulation"
         style="max-width:100%;border:1px solid #ddd;border-radius:6px;">
  </a>
  <figcaption>Velocity field decaying under viscosity (periodic unit square).</figcaption>
</figure>

See this and other cases on the **[iFluid — CFD Examples](/ifluid/)** page.
