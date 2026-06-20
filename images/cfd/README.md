# CFD example animations

Video animations embedded by the Portfolio gallery page (`_pages/ifluid.md`,
served at `/portfolio/`). Each case is shown as serial vs. parallel for two
fields:

| File | Case | Run | Field |
|---|---|---|---|
| `TG-3d-serial-velocity.mp4`     | Taylor–Green 3D   | serial   | velocity |
| `TG-3d-serial-pressure.mp4`     | Taylor–Green 3D   | serial   | pressure |
| `TG-3d-parallel-velocity.mp4`   | Taylor–Green 3D   | parallel | velocity |
| `TG-3d-parallel-pressure.mp4`   | Taylor–Green 3D   | parallel | pressure |
| `ldc2d-serial-velocity.mp4`     | Lid-driven cavity 2D | serial   | velocity |
| `ldc2d-serial-pressure.mp4`     | Lid-driven cavity 2D | serial   | pressure |
| `ldc2d-parallel-velocity.mp4`   | Lid-driven cavity 2D | parallel | velocity |
| `ldc2d-parallel-pressure.mp4`   | Lid-driven cavity 2D | parallel | pressure |

To add or swap an animation, drop the `.mp4` here and reference it from a
`<video><source src="/images/cfd/NAME.mp4" type="video/mp4"></video>` block in
`_pages/ifluid.md`. Keep files small (these are all < 3 MB) for fast loading.
