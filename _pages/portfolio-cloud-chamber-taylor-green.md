---
layout: single
title: "Taylor–Green Vortex (climate)"
permalink: /portfolio/cloud-chamber/taylor-green/
author_profile: true
toc: true
toc_label: "Fields"
toc_sticky: true
---

[← Back to Portfolio](/portfolio/)

Animations produced with the **Cloud-Chamber** solver ported from the
**climate** PR-DNS code. The cases below show the flow fields together with the
thermodynamic and microphysical fields (temperature, supersaturation, cloud
water) that the cloud-chamber model evolves. The 2D fields come from the
Taylor–Green 2D run; the closing velocity vector field is the Taylor–Green 3D
run.

> Animations were generated from the solver's output and rendered in
> **ParaView**. Each clip below loops automatically.

---

## Velocity

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_xvel.gif" alt="Taylor-Green 2D x-velocity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>X-Velocity</strong></figcaption>
  </figure>
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_yvel.gif" alt="Taylor-Green 2D y-velocity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Y-Velocity</strong></figcaption>
  </figure>
</div>

## Vorticity

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_vort.gif" alt="Taylor-Green 2D vorticity"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Vorticity</strong></figcaption>
  </figure>
</div>

## Temperature

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_temperature.gif" alt="Taylor-Green 2D temperature"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Temperature</strong></figcaption>
  </figure>
</div>

## Supersaturation

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_supersat.gif" alt="Taylor-Green 2D supersaturation"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Supersaturation</strong></figcaption>
  </figure>
</div>

## Cloud

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <img src="/images/cfd/TG2d_cloud.gif" alt="Taylor-Green 2D cloud field"
         style="width:100%;border:1px solid #ddd;border-radius:6px;">
    <figcaption style="text-align:center;"><strong>Cloud</strong></figcaption>
  </figure>
</div>

## Velocity Vector Field (3D)

<div style="display:flex;flex-wrap:wrap;gap:1rem;margin:1rem 0;justify-content:center;">
  <figure style="flex:1 1 320px;max-width:480px;margin:0;">
    <video controls autoplay loop muted playsinline preload="metadata" style="width:100%;border:1px solid #ddd;border-radius:6px;">
      <source src="/images/cfd/TG3d_CC_velocity_vector.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="text-align:center;"><strong>Velocity Vector Field</strong></figcaption>
  </figure>
</div>
