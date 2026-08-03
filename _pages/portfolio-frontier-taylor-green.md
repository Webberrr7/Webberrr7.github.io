---
layout: single
title: "Taylor–Green Vortex"
permalink: /portfolio/frontier/taylor-green/
author_profile: true
toc: true
toc_label: "Fields"
toc_sticky: true
---

[← Back to Portfolio](/portfolio/)

A classic **accuracy-verification** problem: an array of counter-rotating
vortices that decays in time under viscosity. The incompressible Navier–Stokes
equations have an *exact analytical solution* for this flow, making it the
standard test for confirming a solver reproduces the correct decay rate and
vortex structure.

**Input file:** max time = 5, max steps = 2000.

For every animation the **serial** run (single process) is placed next to the
**parallel** run (multiple MPI processes) so the two can be compared directly:
a correct parallel implementation must reproduce the serial result. The pairs
below match field-for-field, which is exactly the check used to validate the
MPI/PETSc solver.

> Animations were generated from the solver's output and rendered in
> **ParaView**. Each clip below loops automatically; use the controls to pause
> or scrub.

---

## Velocity Field — Serial vs. Parallel

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-serial-velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong> (1 process)</figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-parallel-velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong> (MPI, 2×2×1)</figcaption>
  </figure>
</div>

## Pressure Field — Serial vs. Parallel

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-serial-pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong> (1 process)</figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-parallel-pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong> (MPI, 2×2×1)</figcaption>
  </figure>
</div>
