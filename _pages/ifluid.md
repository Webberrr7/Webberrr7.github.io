---
layout: single
title: "Portfolio"
permalink: /portfolio/
author_profile: true
toc: true
toc_label: "Examples"
toc_sticky: true
---

A small gallery of incompressible Navier–Stokes simulations I produced with the
**iFluid** incompressible Navier–Stokes solver in the **FronTier++**
front-tracking library (Prof. Xiaolin Li's group, Stony Brook University).
Each animation below is a standard CFD verification case, so the results can be
checked at a glance against the well-known reference behavior.

> All animations were generated from the solver's output, visualized in
> **ParaView**, and exported to GIF. Click any animation to view it full size.

---

## Taylor–Green Vortex

A classic **accuracy-verification** problem: an array of counter-rotating
vortices that decays in time under viscosity. The 2-D incompressible
Navier–Stokes equations have an *exact analytical solution* for this flow, so it
is the standard test for confirming that a solver reproduces the correct decay
rate and vortex structure.

- **Domain / BCs:** periodic unit square
- **What to look for:** the four-vortex pattern stays symmetric while the
  velocity magnitude decays smoothly and monotonically — matching the analytical
  exponential decay.

<figure>
  <a href="/images/cfd/taylor-green.gif">
    <img src="/images/cfd/taylor-green.gif" alt="Taylor–Green vortex simulation"
         style="max-width:100%;border:1px solid #ddd;border-radius:6px;">
  </a>
  <figcaption>Taylor–Green vortex: velocity field decaying under viscosity.</figcaption>
</figure>

---

## Lid-Driven Cavity

The most widely used **benchmark** for incompressible flow solvers. Fluid sits
in a square cavity whose top wall (the "lid") slides at constant velocity,
driving a large primary vortex in the center plus smaller counter-rotating
vortices in the bottom corners. Results are conventionally compared against the
Ghia, Ghia & Shin (1982) reference data.

- **Domain / BCs:** unit square, moving top lid, no-slip on the other three walls
- **What to look for:** a single primary circulation centered slightly toward the
  top-right, with secondary vortices forming in the lower corners as the Reynolds
  number increases.

<figure>
  <a href="/images/cfd/lid-driven-cavity.gif">
    <img src="/images/cfd/lid-driven-cavity.gif" alt="Lid-driven cavity simulation"
         style="max-width:100%;border:1px solid #ddd;border-radius:6px;">
  </a>
  <figcaption>Lid-driven cavity: streamlines / velocity field reaching steady state.</figcaption>
</figure>

---

*More iFluid cases (Rayleigh–Taylor instability, flow past a sphere, vortex
shedding) coming soon.*
