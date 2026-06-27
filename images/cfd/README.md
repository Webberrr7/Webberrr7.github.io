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
PP = PR-DNS parallel. PR-DNS now writes 48 frames for both serial and parallel
(FronTierCpp writes 708 frames).

| File | Config | Field |
|---|---|---|
| `ldc2d_PS_velocity.mp4` | PR-DNS serial        | velocity |
| `ldc2d_PS_pressure.mp4` | PR-DNS serial        | pressure |
| `ldc2d_PP_velocity.mp4` | PR-DNS parallel      | velocity |
| `ldc2d_PP_pressure.mp4` | PR-DNS parallel      | pressure |
| `ldc2d_FS_velocity.mp4` | FronTierCpp serial   | velocity |
| `ldc2d_FS_pressure.mp4` | FronTierCpp serial   | pressure |
| `ldc2d_FP_velocity.mp4` | FronTierCpp parallel | velocity |
| `ldc2d_FP_pressure.mp4` | FronTierCpp parallel | pressure |

To add or swap an animation, drop the `.mp4` here and reference it from a
`<video><source src="/images/cfd/NAME.mp4" type="video/mp4"></video>` block in
`_pages/ifluid.md`. Keep files small for fast loading (these range ~0.2–8 MB).
