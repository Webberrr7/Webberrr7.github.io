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
walls** — the reduced-Ra configuration of the BNL convection cloud chamber
Case 3, computed
with the particle-resolved DNS code built on **FronTier++** (incompressible
Navier–Stokes, projection method, Crank–Nicolson scalars).

- **Walls:** bottom 285.95 K, top 282.95 K, four sides 282.93–285.76 K — a 3 K
  vertical difference, scaled from convection cloud chamber Case 3 about
  T₀ = 284.45 K
- **Air:** ν = 1.5×10⁻⁵ m²/s, α = 1.9×10⁻⁵ m²/s → **Ra ≈ 4.5×10⁷**, **Pr ≈ 0.79**
  (free-fall velocity 0.227 m/s, free-fall time ≈ 2.2 s); started from rest with
  a small temperature perturbation
- **Output:** frames every 5 s

The case was run at two resolutions. Both advance at advective CFL = 0.75 to
t = 300 s; they differ only in grid and cost:

|  | **128³** | **256³** |
|---|---|---|
| Grid spacing | h = 3.9 mm | h = 1.95 mm |
| Decomposition | 4×4×4, 64 ranks on 1 Perlmutter node | 8×8×8, 512 ranks on 8 nodes |
| Time step | Δt ≈ 0.0135 s | Δt ≈ 0.0070 s |
| Steps | 21,800 at 1.47 s/step | 42,882 at 1.91 s/step |
| Cost | ≈ 9 node-hours | 22 h 45 min wall, ≈ 182 node-hours |

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

### Scaling

How the solver scales on **Perlmutter** (64 ranks per node): **weak scaling**
holds the work per rank fixed at 32³ or 64³ cells while adding ranks; **strong
scaling** holds the total grid fixed at 128³ or 256³ and divides it over more
ranks.

The four series:

| Series | Held fixed | Varied | Range | Points |
|---|---|---|---|---|
| Strong, 128³ | total grid 128³ | cells per rank shrink | 8 → 512 ranks (64³ → 16³ cells/rank) | 5 |
| Strong, 256³ | total grid 256³ | cells per rank shrink | 64 → 1024 ranks (64³ → 16³ cells/rank) | 5 |
| Weak, 32³/rank | 32³ cells per rank | total grid grows with ranks | 8 → 1000 ranks (grid 64³ → 320³) | 8 |
| Weak, 64³/rank | 64³ cells per rank | total grid grows with ranks | 1 → 512 ranks (grid 64³ → 512³) | 8 |



<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:640px;margin:0;">
    <a href="/images/cfd/chamber3d_scaling_strong.png">
      <img src="/images/cfd/chamber3d_scaling_strong.png" alt="Strong scaling: time per step vs. MPI ranks"
           style="width:100%;border:1px solid #ddd;border-radius:6px;">
    </a>
    <figcaption style="text-align:center;"><strong>Strong scaling</strong> — time per step at fixed total grid (128³, 256³)</figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:640px;margin:0;">
    <a href="/images/cfd/chamber3d_scaling_weak.png">
      <img src="/images/cfd/chamber3d_scaling_weak.png" alt="Weak scaling: time per step at fixed cells per rank"
           style="width:100%;border:1px solid #ddd;border-radius:6px;">
    </a>
    <figcaption style="text-align:center;"><strong>Weak scaling</strong> — time per step at fixed cells per rank (32³, 64³)</figcaption>
  </figure>
</div>

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:640px;margin:0;">
    <a href="/images/cfd/chamber3d_scaling_per_routine.png">
      <img src="/images/cfd/chamber3d_scaling_per_routine.png" alt="Per-routine time per step for all four series"
           style="width:100%;border:1px solid #ddd;border-radius:6px;">
    </a>
    <figcaption style="text-align:center;"><strong>Per-routine time per step</strong> — all four series</figcaption>
  </figure>
</div>

Per-routine timings, in seconds per time step:

<div style="overflow-x:auto;" markdown="1">

| Series | Ranks | Nodes | Ranks/node | Cells/rank | Projection | Diffusion | Advection | Front propagate | Temperature solve | Vapor solve | Remainder | Whole step |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| w32 | 8 | 1 | 8 | 32768 | 0.09183 | 0.1051 | 0.3755 | 0.3854 | 0.03078 | 0.03158 | 0.02368 | 1.044 |
| w32 | 27 | 1 | 27 | 32768 | 0.1533 | 0.1731 | 0.4278 | 0.4585 | 0.06017 | 0.05455 | 0.02680 | 1.354 |
| w32 | 64 | 1 | 64 | 32768 | 0.2245 | 0.2598 | 0.4446 | 0.5020 | 0.1040 | 0.09011 | 0.03430 | 1.659 |
| w32 | 125 | 2 | 62.5 | 32768 | 0.2549 | 0.4260 | 0.5666 | 0.4646 | 0.1604 | 0.1383 | 0.03142 | 2.042 |
| w32 | 216 | 4 | 54 | 32768 | 0.3167 | 0.4906 | 0.5130 | 0.4626 | 0.1717 | 0.1388 | 0.03316 | 2.127 |
| w32 | 343 | 6 | 57.17 | 32768 | 0.3910 | 0.5250 | 0.4583 | 0.4703 | 0.1880 | 0.1498 | 0.03560 | 2.218 |
| w32 | 512 | 8 | 64 | 32768 | 0.4635 | 0.5563 | 0.4997 | 0.5042 | 0.2084 | 0.1612 | 0.03824 | 2.432 |
| w32 | 1000 | 16 | 62.5 | 32768 | 1.240 | 0.6248 | 0.6682 | 0.5556 | 0.2422 | 0.1887 | 0.04041 | 3.560 |
| w64 | 1 | 1 | 1 | 262144 | 0.5717 | 0.6012 | 2.898 | 1.736 | 0.1623 | 0.1659 | 0.1923 | 6.327 |
| w64 | 8 | 1 | 8 | 262144 | 0.7301 | 1.387 | 2.912 | 1.535 | 0.5435 | 0.5294 | 0.1466 | 7.783 |
| w64 | 27 | 1 | 27 | 262144 | 1.606 | 5.267 | 3.350 | 1.916 | 1.730 | 1.633 | 0.1718 | 15.67 |
| w64 | 64 | 1 | 64 | 262144 | 3.020 | 7.114 | 3.413 | 2.157 | 2.192 | 1.936 | 0.1956 | 20.03 |
| w64 | 125 | 2 | 62.5 | 262144 | 3.077 | 7.524 | 3.424 | 1.936 | 2.416 | 2.128 | 0.2003 | 20.71 |
| w64 | 216 | 4 | 54 | 262144 | 2.876 | 7.545 | 3.572 | 1.988 | 2.536 | 2.202 | 0.2357 | 20.96 |
| w64 | 343 | 6 | 57.17 | 262144 | 3.774 | 8.726 | 3.927 | 1.953 | 2.936 | 2.456 | 0.2132 | 23.99 |
| w64 | 512 | 8 | 64 | 262144 | 4.172 | 9.395 | 4.432 | 2.186 | 2.994 | 2.503 | 0.2583 | 25.94 |
| s128 | 8 | 1 | 8 | 262144 | 0.7301 | 1.387 | 2.912 | 1.535 | 0.5435 | 0.5294 | 0.1466 | 7.783 |
| s128 | 64 | 1 | 64 | 32768 | 0.2245 | 0.2598 | 0.4446 | 0.5020 | 0.1040 | 0.09011 | 0.03430 | 1.659 |
| s128 | 128 | 2 | 64 | 16384 | 0.1636 | 0.1332 | 0.2251 | 0.3445 | 0.06381 | 0.05113 | 0.02086 | 1.002 |
| s128 | 256 | 4 | 64 | 8192 | 0.1582 | 0.07274 | 0.1157 | 0.2354 | 0.04016 | 0.03006 | 0.01312 | 0.6654 |
| s128 | 512 | 8 | 64 | 4096 | 0.2120 | 0.04965 | 0.08263 | 0.1970 | 0.02889 | 0.01961 | 0.01146 | 0.6013 |
| s256 | 64 | 1 | 64 | 262144 | 3.014 | 7.113 | 3.420 | 2.158 | 2.185 | 1.919 | 0.1919 | 20.00 |
| s256 | 128 | 2 | 64 | 131072 | 1.476 | 3.123 | 1.822 | 1.391 | 0.9705 | 0.8161 | 0.1200 | 9.719 |
| s256 | 256 | 4 | 64 | 65536 | 0.7501 | 1.317 | 1.017 | 0.8494 | 0.4384 | 0.3518 | 0.05975 | 4.783 |
| s256 | 512 | 8 | 64 | 32768 | 0.4635 | 0.5563 | 0.4997 | 0.5042 | 0.2084 | 0.1612 | 0.03824 | 2.432 |
| s256 | 1024 | 16 | 64 | 16384 | 1.145 | 0.2989 | 0.3119 | 0.3385 | 0.1245 | 0.08863 | 0.02703 | 2.335 |

</div>

Download: [chamber3d-scaling-table.csv](/files/chamber3d-scaling-table.csv)
