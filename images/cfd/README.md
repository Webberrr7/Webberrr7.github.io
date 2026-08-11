# CFD example animations

Animations embedded by the Portfolio child pages. `/portfolio/` itself is a hub
page and embeds no media — each group below lives on exactly one child page.

| Page | Source file |
|---|---|
| `/portfolio/frontier/taylor-green/`     | `_pages/portfolio-frontier-taylor-green.md` |
| `/portfolio/frontier/ldc2d/`            | `_pages/portfolio-frontier-ldc2d.md` |
| `/portfolio/cloud-chamber/particle-2d/` | `_pages/portfolio-cloud-chamber-particle-2d.md` |
| `/portfolio/cloud-chamber/taylor-green/`| `_pages/portfolio-cloud-chamber-taylor-green.md` |
| `/portfolio/cloud-chamber/rayleigh-benard/` | `_pages/portfolio-cloud-chamber-rayleigh-benard.md` |

## Taylor–Green Vortex (3D) — serial vs. parallel

Page: `/portfolio/frontier/taylor-green/`

| File | Run | Field |
|---|---|---|
| `TG-3d-serial-velocity.mp4`   | serial   | velocity |
| `TG-3d-serial-pressure.mp4`   | serial   | pressure |
| `TG-3d-parallel-velocity.mp4` | parallel | velocity |
| `TG-3d-parallel-pressure.mp4` | parallel | pressure |

## Lid-Driven Cavity (2D) — FronTierCpp serial vs. parallel

Page: `/portfolio/frontier/ldc2d/`

FS = FronTierCpp serial, FP = FronTierCpp parallel, FPH = FronTierCpp parallel
on BNL's hpc1 cluster. The FS and FP runs advanced to step 10000 and wrote 708
output frames. Each run shows the velocity vector field alongside the pressure
field; FPH contributes a velocity field only.

| File | Config | Field |
|---|---|---|
| `ldc2d_FS_velocity_vector.mp4` | FronTierCpp serial        | velocity vector field |
| `ldc2d_FS_pressure.mp4`        | FronTierCpp serial        | pressure |
| `ldc2d_FP_velocity_vector.mp4` | FronTierCpp parallel      | velocity vector field |
| `ldc2d_FP_pressure.mp4`        | FronTierCpp parallel      | pressure |
| `ldc2d_FPH_velocity.mp4`       | FronTierCpp parallel/hpc1 | velocity field |

## Cloud Chamber (ported from the climate PR-DNS code)

Pages: `/portfolio/cloud-chamber/taylor-green/` (TG2d + TG3d),
`/portfolio/cloud-chamber/particle-2d/` (particle2d), and
`/portfolio/cloud-chamber/rayleigh-benard/` (rbconv).

| File | Case | Field |
|---|---|---|
| `TG2d_xvel.gif`        | Taylor–Green 2D | x-velocity |
| `TG2d_yvel.gif`        | Taylor–Green 2D | y-velocity |
| `TG2d_vort.gif`        | Taylor–Green 2D | vorticity |
| `TG2d_temperature.gif` | Taylor–Green 2D | temperature |
| `TG2d_supersat.gif`    | Taylor–Green 2D | supersaturation |
| `TG2d_cloud.gif`       | Taylor–Green 2D | cloud |
| `particle2d_vort.gif`        | Particles 2D | vorticity |
| `particle2d_temperature.gif` | Particles 2D | temperature |
| `particle2d_supersat.gif`    | Particles 2D | supersaturation |
| `TG3d_CC_velocity_vector.mp4` | Taylor–Green 3D | velocity vector field |
| `rbconv_xvel.mp4`        | Rayleigh–Bénard convection | x-velocity |
| `rbconv_yvel.mp4`        | Rayleigh–Bénard convection | y-velocity |
| `rbconv_temperature.mp4` | Rayleigh–Bénard convection | temperature |

To add or swap an animation, drop the file here and reference it from a
`<video><source src="/images/cfd/NAME.mp4" type="video/mp4"></video>` block (or
an `<img>` for a GIF) in the relevant child page above. Keep files small for
fast loading (these range ~0.2–8 MB).
