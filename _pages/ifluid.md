---
layout: single
title: "Portfolio"
permalink: /portfolio/
author_profile: true
toc: true
toc_label: "Examples"
toc_sticky: true
---

A gallery of incompressible Navier–Stokes simulations I produced with the
**iFluid** solver in the **FronTier++** front-tracking library (Prof. Xiaolin
Li's group, Stony Brook University). Each case is a standard CFD verification
problem, shown for both the **velocity** and **pressure** fields.

For every animation the **serial** run (single process) is placed next to the
**parallel** run (multiple MPI processes) so the two can be compared directly:
a correct parallel implementation must reproduce the serial result. The pairs
below match field-for-field, which is exactly the check used to validate the
MPI/PETSc solver.

> Animations were generated from the solver's output and rendered in
> **ParaView**. Each pair below loops automatically; use the controls to pause
> or scrub.

---

## Taylor–Green Vortex (3D)

A classic **accuracy-verification** problem: an array of counter-rotating
vortices that decays in time under viscosity. The incompressible Navier–Stokes
equations have an *exact analytical solution* for this flow, making it the
standard test for confirming a solver reproduces the correct decay rate and
vortex structure.

**Input file:** max time = 5, max steps = 2000.

**Velocity field — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-serial-velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong> (1 process)</figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-parallel-velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong> (MPI, 2×2×1)</figcaption>
  </figure>
</div>

**Pressure field — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-serial-pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong> (1 process)</figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG-3d-parallel-pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong> (MPI, 2×2×1)</figcaption>
  </figure>
</div>

---

## Lid-Driven Cavity (2D)

The most widely used **benchmark** for incompressible flow solvers: fluid in a
square cavity whose top wall (the "lid") slides at constant velocity, driving a
large primary vortex plus smaller counter-rotating vortices in the bottom
corners. Run with the **FronTierCpp** solver in both serial and parallel
(serial above parallel) so the two runs can be compared directly: a correct
parallel implementation must reproduce the serial result.

### FronTierCpp — Serial (FS)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FS_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FS_pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Pressure</strong></figcaption>
  </figure>
</div>

### FronTierCpp — Parallel (FP)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FP_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FP_pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Pressure</strong></figcaption>
  </figure>
</div>

### FronTierCpp — Parallel on hpc1 (BNL cluster) (FPH)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FPH_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Field</strong> — animation from a parallel FronTierCpp run on BNL's hpc1 cluster</figcaption>
  </figure>
</div>

---

## Cloud Chamber

Animations produced with the **Cloud-Chamber** solver ported from the
**climate** PR-DNS code. The cases below show the flow fields together with the
thermodynamic and microphysical fields (temperature, supersaturation, cloud
water) that the cloud-chamber model evolves.

### Taylor–Green (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_xvel.gif" alt="Taylor-Green 2D x-velocity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>X-Velocity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_yvel.gif" alt="Taylor-Green 2D y-velocity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Y-Velocity</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_vort.gif" alt="Taylor-Green 2D vorticity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Vorticity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_temperature.gif" alt="Taylor-Green 2D temperature"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Temperature</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_supersat.gif" alt="Taylor-Green 2D supersaturation"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Supersaturation</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/TG2d_cloud.gif" alt="Taylor-Green 2D cloud field"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Cloud</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:0 1 480px;margin:0;">
    <img src="/images/cfd/TG2d_comp.gif" alt="Taylor-Green 2D component field"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Component</strong></figcaption>
  </figure>
</div>

### Particles (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/particle2d_vort.gif" alt="Particle 2D vorticity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Vorticity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/particle2d_temperature.gif" alt="Particle 2D temperature"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Temperature</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/particle2d_supersat.gif" alt="Particle 2D supersaturation"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Supersaturation</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;margin:0;">
    <img src="/images/cfd/particle2d_comp.gif" alt="Particle 2D component field"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Component</strong></figcaption>
  </figure>
</div>

### Taylor–Green (3D) — Velocity Vector Field

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:0 1 480px;margin:0;">
    <video controls muted loop autoplay playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG3d_CC_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
</div>

---

*More iFluid cases (Rayleigh–Taylor instability, flow past a sphere, vortex
shedding) coming soon.*
