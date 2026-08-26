---
layout: single
title: "Portfolio"
permalink: /portfolio/
author_profile: true
toc: true
toc_label: "Projects"
toc_sticky: true
---

A gallery of incompressible Navier–Stokes simulations I produced with the
**iFluid** solver in the **FronTier++** front-tracking library (Prof. Xiaolin
Li's group, Stony Brook University). Each case is a standard CFD verification
problem, shown for both the **velocity** and **pressure** fields.

---

## FronTier

FronTier is a set of libraries implementing front-tracking algorithms — a
numerical method for solving partial differential equations whose solutions
contain discontinuities. It was developed at Stony Brook University and is
distributed under the GNU LGPL. My work is based primarily on the iFluid
module, its incompressible Navier–Stokes solver.

### [Taylor–Green Vortex](/portfolio/frontier/taylor-green/)

The 3D vortex-decay accuracy benchmark, with the serial run placed next to the
parallel run for both the velocity and pressure fields.

### [Lid-Driven Cavity (LDC2D)](/portfolio/frontier/ldc2d/)

The FronTierCpp solver in three configurations — serial, parallel, and parallel
on BNL's hpc1 cluster — grouped by velocity and pressure.

---

## Cloud Chamber

Cloud Chamber extends FronTier by porting Zheng Gao's climate module onto the
current FronTier++ code base for particle-resolved cloud microphysics. Ongoing
work replaces the periodic scalar boundary conditions with a Dirichlet (fixed
wall temperature and vapor) formulation.

### [Particle 2D](/portfolio/cloud-chamber/particle-2d/)

Vorticity, temperature, and supersaturation fields from the particle-resolved
2D run.

### [Taylor–Green Vortex (climate)](/portfolio/cloud-chamber/taylor-green/)

Taylor–Green driven flow through the cloud-chamber model: velocity, vorticity,
and the thermodynamic and microphysical fields, plus a 3D velocity vector field.

### [Rayleigh–Bénard Convection](/portfolio/cloud-chamber/rayleigh-benard/)

Buoyancy-driven convection between a heated bottom wall and a cooled top wall,
exercising the Dirichlet boundary formulation: velocity and temperature fields,
in both 2D and 3D.

### [Chamber](/portfolio/cloud-chamber/chamber/)

The chamber with the periodic side boundaries replaced by Dirichlet
(fixed-temperature) walls — every boundary prescribed. Velocity, temperature,
and velocity vector fields, serial vs. parallel, in both 2D and 3D.

---

*More iFluid cases (Rayleigh–Taylor instability, flow past a sphere, vortex
shedding) coming soon.*
