---
layout: single
title: "Chamber"
permalink: /portfolio/cloud-chamber/chamber/
redirect_from:
  - /portfolio/cloud-chamber/chamber-2d/
author_profile: true
toc: true
toc_label: "Fields"
toc_sticky: true
---

[← Back to Portfolio](/portfolio/)

Animations produced with the **Cloud-Chamber** solver ported from the
**climate** PR-DNS code. The chamber case replaces the periodic side
boundaries of the Rayleigh–Bénard run with **Dirichlet** (fixed-temperature)
side walls, so every boundary holds a prescribed temperature. Each field is
shown for the **serial** run next to the **parallel** run so the two can be
compared directly.

The 2D run:

- **Wall temperatures:** lower 270.75 K, upper 269.25 K, side walls 270 K
- **Input file:** max time = 300, max steps = 5000

---

## X-Velocity (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_xvel_serial.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_xvel_parallel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

## Y-Velocity (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_yvel_serial.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_yvel_parallel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

## Temperature (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_temperature_serial.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_temperature_parallel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

## Velocity Vector Field (2D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_vector_velocity_serial.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber2d_vector_velocity_parallel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

## 3D Run

The same chamber extended to **three dimensions**, with **Dirichlet**
(constant-state) conditions on all six walls: zero velocity, and a fixed
temperature — heated bottom, cooled top, all other walls at 270 K.

- **Domain:** [0, 2] × [0, 1] × [0, 1]
- **Computational grid:** 128 × 64 × 64
- **Wall temperatures:** bottom (y-lower) 270.75 K, top (y-upper) 269.25 K,
  all four side walls 270 K
- **Input file:** max time = 300, max steps = 5000

**Velocity vector field — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_vector_velocity_serial.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_vector_velocity_parallel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

**Temperature (Z-slice) — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_serial_tz.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_parallel_tz.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

**Temperature (X-slice) — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_serial_tx.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_parallel_tx.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

## 3D Box Run

A second 3D configuration in a **box** geometry, again with **Dirichlet**
conditions on every wall, run in **serial** and **parallel**: the velocity
field, plus temperature slices normal to each of the three axes.

**Velocity — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_serial_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_parallel_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

**Temperature (X-slice) — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_serial_temperature_xslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_parallel_temperature_xslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

**Temperature (Y-slice) — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_serial_temperature_yslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_parallel_temperature_yslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>

**Temperature (Z-slice) — serial vs. parallel**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_serial_temperature_zslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Serial</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d_box_parallel_temperature_zslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Parallel</strong></figcaption>
  </figure>
</div>
