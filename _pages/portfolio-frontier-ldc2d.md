---
layout: single
title: "Lid-Driven Cavity (LDC2D)"
permalink: /portfolio/frontier/ldc2d/
author_profile: true
toc: true
toc_label: "Fields"
toc_sticky: true
---

[← Back to Portfolio](/portfolio/)

The most widely used **benchmark** for incompressible flow solvers: fluid in a
square cavity whose top wall (the "lid") slides at constant velocity, driving a
large primary vortex plus smaller counter-rotating vortices in the bottom
corners. Run with the **FronTierCpp** solver in both serial and parallel
(serial alongside parallel) so the two runs can be compared directly: a correct
parallel implementation must reproduce the serial result.

> Animations were generated from the solver's output and rendered in
> **ParaView**. Each clip below loops automatically; use the controls to pause
> or scrub.

---

## Velocity

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FS_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>FronTierCpp — Serial (FS)</strong><br>Velocity Vector Field</figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FP_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>FronTierCpp — Parallel (FP)</strong><br>Velocity Vector Field</figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FPH_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>FronTierCpp — Parallel on hpc1 (BNL cluster) (FPH)</strong><br>Velocity Field</figcaption>
  </figure>
</div>

## Pressure

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FS_pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>FronTierCpp — Serial (FS)</strong><br>Pressure</figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/ldc2d_FP_pressure.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>FronTierCpp — Parallel (FP)</strong><br>Pressure</figcaption>
  </figure>
</div>
