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

## Lid-Driven Cavity (2D) — solver comparison

Four configurations of the same 2D lid-driven cavity test case:
FS = FronTierCpp serial, FP = FronTierCpp parallel, PS = PR-DNS serial,
PP = PR-DNS parallel. PP has **no file** — that run diverged numerically at the
second time step, so no animation could be produced.

| File | Config | Field |
|---|---|---|
| `ldc2d_PS_velocity.mp4` | PR-DNS serial      | velocity |
| `ldc2d_PS_pressure.mp4` | PR-DNS serial      | pressure |
| `ldc2d_FS_velocity.mp4` | FronTierCpp serial | velocity |
| `ldc2d_FS_pressure.mp4` | FronTierCpp serial | pressure |
| `ldc2d_FP_velocity.mp4` | FronTierCpp parallel | velocity |
| `ldc2d_FP_pressure.mp4` | FronTierCpp parallel | pressure |

To add or swap an animation, drop the `.mp4` here and reference it from a
`<video><source src="/images/cfd/NAME.mp4" type="video/mp4"></video>` block in
`_pages/ifluid.md`. Keep files small for fast loading — most are < 1 MB, but the
PR-DNS serial (PS) files are large (~28 MB pressure, ~50 MB velocity) because
PR-DNS wrote 10000 frames. Consider compressing those if page load is slow.
