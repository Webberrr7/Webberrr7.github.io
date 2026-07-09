# CFD example animations

Video animations embedded by the Portfolio gallery page (`_pages/ifluid.md`,
served at `/portfolio/`).

## Taylor–Green Vortex (3D) — serial vs. parallel

| File | Run | Field |
|---|---|---|
| `TG-3d-serial-velocity.mp4`   | serial   | velocity |
| `TG-3d-serial-pressure.mp4`   | serial   | pressure |
| `TG-3d-parallel-velocity.mp4` | parallel | velocity |
| `TG-3d-parallel-pressure.mp4` | parallel | pressure |

## Lid-Driven Cavity (2D) — FronTierCpp serial vs. parallel

FS = FronTierCpp serial, FP = FronTierCpp parallel. Both runs advanced to step
10000 and wrote 708 output frames. Each run shows the velocity vector field
alongside the pressure field.

| File | Config | Field |
|---|---|---|
| `ldc2d_FS_velocity_vector.mp4` | FronTierCpp serial   | velocity vector field |
| `ldc2d_FS_pressure.mp4`        | FronTierCpp serial   | pressure |
| `ldc2d_FP_velocity_vector.mp4` | FronTierCpp parallel | velocity vector field |
| `ldc2d_FP_pressure.mp4`        | FronTierCpp parallel | pressure |

To add or swap an animation, drop the `.mp4` here and reference it from a
`<video><source src="/images/cfd/NAME.mp4" type="video/mp4"></video>` block in
`_pages/ifluid.md`. Keep files small for fast loading (these range ~0.2–8 MB).
