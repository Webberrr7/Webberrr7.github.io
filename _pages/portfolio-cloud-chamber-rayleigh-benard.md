---
layout: single
title: "Rayleigh–Bénard Convection"
permalink: /portfolio/cloud-chamber/rayleigh-benard/
author_profile: true
toc: true
toc_label: "Fields"
toc_sticky: true
---

[← Back to Portfolio](/portfolio/)

Animations produced with the **Cloud-Chamber** solver ported from the
**climate** PR-DNS code. Rayleigh–Bénard convection — fluid heated from below
and cooled from above — is the canonical buoyancy-driven flow. The run uses
**periodic** boundary conditions at the left and right sides, and a
**Dirichlet** (fixed wall) condition at the top and bottom.

---

## Velocity (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rbconv_xvel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>X-Velocity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rbconv_yvel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Y-Velocity</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rbconv_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
</div>

## Temperature (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rbconv_temperature.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature</strong></figcaption>
  </figure>
</div>

## 3D Run

The same convection case extended to **three dimensions**: the velocity vector
field, plus temperature slices normal to the Y and Z axes.

- **Rayleigh number:** Ra = 10000
- **Computational grid:** 128 × 64 × 8
- **Wall temperatures:** lower 270.75 K, upper 269.25 K
- **Input file:** max time = 1200, max steps = 20000

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rb_3d_vector_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rb_3d_Yslice_temperature.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature — Y-Slice</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rb_3d_Zslice_temperature.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature — Z-Slice</strong></figcaption>
  </figure>
</div>
