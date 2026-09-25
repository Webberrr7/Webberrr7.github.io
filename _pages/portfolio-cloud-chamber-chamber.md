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
side walls, so every boundary holds a prescribed temperature. Each 2D field is
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

<a id="chamber3d128"></a>

## chamber3d

Dry Rayleigh–Bénard convection in a **0.5 m cubic cavity with six isothermal
walls** — the reduced-Ra configuration of the BNL Π-Chamber Case 3, computed
with the particle-resolved DNS code built on **FronTier++** (incompressible
Navier–Stokes, projection method, Crank–Nicolson scalars).

- **Walls:** bottom 285.95 K, top 282.95 K, four sides 282.93–285.76 K — a 3 K
  vertical difference, scaled from Π-Chamber Case 3 about T₀ = 284.45 K
- **Air:** ν = 1.5×10⁻⁵ m²/s, α = 1.9×10⁻⁵ m²/s → **Ra ≈ 4.5×10⁷**, **Pr ≈ 0.79**
  (free-fall velocity 0.227 m/s, free-fall time ≈ 2.2 s); started from rest with
  a small temperature perturbation
- **Output:** frames every 5 s

The case was run at two resolutions. Both advance at advective CFL = 0.75 to
t = 300 s; they differ only in grid, cost, and colour scale:

|  | **128³** | **256³** |
|---|---|---|
| Grid spacing | h = 3.9 mm | h = 1.95 mm |
| Decomposition | 4×4×4, 64 ranks on 1 Perlmutter node | 8×8×8, 512 ranks on 8 nodes |
| Time step | Δt ≈ 0.0135 s | Δt ≈ 0.0070 s |
| Steps | 21,800 at 1.47 s/step | 42,882 at 1.91 s/step |
| Cost | ≈ 9 node-hours | 22 h 45 min wall, ≈ 182 node-hours |
| Colour scale | temperature fixed to the wall range 282.9–286.0 K | fixed to the last frame's range: T 282.94–285.92 K, \|u\| 0–0.134 m/s |

### 128³

**Velocity and temperature (X-slice)**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d128_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d128_temperature_xslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (X-slice)</strong></figcaption>
  </figure>
</div>

**Temperature — Y- and Z-slices**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d128_temperature_yslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (Y-slice)</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d128_temperature_zslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (Z-slice)</strong></figcaption>
  </figure>
</div>

### 256³

**Velocity and temperature (X-slice)**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d256_velocity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d256_temperature_xslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (X-slice)</strong></figcaption>
  </figure>
</div>

**Temperature — Y- and Z-slices**

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d256_temperature_yslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (Y-slice)</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/chamber3d256_temperature_zslice.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature (Z-slice)</strong></figcaption>
  </figure>
</div>
