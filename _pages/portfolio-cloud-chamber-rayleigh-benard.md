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
and cooled from above — is the canonical buoyancy-driven flow, and here it
exercises the Dirichlet (fixed wall temperature) boundary formulation.

> Animations were generated from the solver's output and rendered in
> **ParaView**. Each clip below loops automatically; use the controls to pause
> or scrub.

---

## Velocity

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

## Temperature

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/rbconv_temperature.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Temperature</strong></figcaption>
  </figure>
</div>
