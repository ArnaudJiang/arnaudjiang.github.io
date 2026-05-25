---
layout: post
title: "Tokamak vs Stellarator: Two Ways to Twist Magnetic Fields"
date: 2026-05-25 00:00:00 +0800
categories: plasma fusion stellarator
permalink: /plasma-fusion/tokamak-vs-stellarator/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 14
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/tokamak-vs-stellarator/
description: "Not a catalog comparison, but a question of how to make field lines behave."
excerpt: "Not a catalog comparison, but a question of how to make field lines behave."
---

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/tokamak-vs-stellarator/" | relative_url }}">中文</a></p>

[Back to Plasma & Fusion series]({{ "/plasma-fusion/" | relative_url }})

# Tokamak vs Stellarator: Two Ways to Twist Magnetic Fields

## Not a catalog comparison, but a question of how to make field lines behave

Tokamaks and stellarators are often compared as two reactor types.

That is useful, but it can hide the deeper question.

Both are attempts to solve the same geometric problem:

> how do we make magnetic field lines wrap around a torus in a way that confines plasma?

The difference is not simply shape.

It is where the twist comes from.

---

## 1. Why field lines need twist

A purely toroidal magnetic field is not enough.

Particles experience curvature and grad-$B$ drifts. Without a compensating geometry, these drifts create charge separation and outward motion.

Field lines need poloidal motion as well as toroidal motion. They must wind around the torus helically, sampling different regions so drifts can average out.

This helical winding is the shared goal.

Tokamaks and stellarators differ in how they create it.

---

## 2. Tokamak: let the plasma carry the twist

A tokamak uses a strong toroidal field from external coils and a large plasma current to create a poloidal field.

Together, these fields create helical magnetic field lines.

The beauty of the tokamak is symmetry.

The device is approximately axisymmetric. That symmetry helps confinement, simplifies equilibrium, and gives strong theoretical and computational tools.

But the plasma current is both useful and dangerous.

It creates needed twist.
It also creates current-driven instabilities, disruptions, and pulsed-operation challenges unless non-inductive current drive is used.

The tokamak bargain is:

> simpler geometry, but a more central plasma current problem.

---

## 3. Stellarator: build the twist into the coils

A stellarator tries to create the needed helical field mostly with external three-dimensional coils.

The plasma does not need to carry a large toroidal current to make the basic confining geometry.

This gives stellarators a major conceptual advantage:

steady-state operation becomes more natural, and some current-driven disruption risks can be reduced.

But the price is geometry.

The coils are complex. The magnetic field is three-dimensional. Equilibrium, transport, and optimization become much harder.

The stellarator bargain is:

> less reliance on plasma current, but a much harder geometry problem.

---

## 4. Axisymmetry versus three-dimensional design

Tokamak axisymmetry is powerful.

It gives a conserved canonical momentum that helps particle confinement. It reduces the equilibrium problem. It makes diagnostics, modeling, and engineering more regular.

Stellarators give up axisymmetry.

That sounds like a loss, and it is. But a carefully designed 3D field can still have good confinement if it approximates useful symmetries in the right coordinates. This is where ideas such as quasisymmetry enter.

The stellarator does not ask:

> can we keep the machine simple?

It asks:

> can we design enough hidden order into a complicated magnetic field?

---

## 5. Stability and disruptions

Tokamaks can achieve excellent confinement, but large plasma current creates disruption risk. A disruption is a rapid loss of confinement and current, with large mechanical and thermal loads.

This is one of the central tokamak engineering challenges.

Stellarators, by reducing dependence on large plasma current, can avoid some disruption mechanisms. That does not make them automatically stable. They still face pressure-driven modes, islands, neoclassical transport, turbulence, and edge issues.

The contrast is not:

> tokamaks unstable, stellarators stable.

It is:

> tokamaks and stellarators expose different stability problems.

---

## 6. Transport tradeoffs

Tokamaks benefit from symmetry, but turbulent transport remains a major issue.

Stellarators historically suffered from neoclassical transport because trapped particles in 3D fields could drift radially. Modern stellarators use optimization to reduce this loss.

This is why the stellarator story changed with computation.

The old stellarator was a clever magnetic idea.
The modern stellarator is a numerical design object.

Its geometry is chosen not merely to make field lines close nicely, but to reduce particle losses, improve MHD behavior, manage islands, and satisfy coil constraints.

---

## 7. Engineering personality

Tokamaks concentrate difficulty in plasma control, current drive, disruption avoidance, and exhaust.

Stellarators move difficulty into coil geometry, manufacturing tolerances, 3D optimization, and configuration design.

Both still face materials, tritium breeding, heating, diagnostics, maintenance, and economics.

So the question is not which concept is easy.

Neither is easy.

The question is:

> where do we want the difficulty to live?

---

## Closing

Tokamaks and stellarators are not rival slogans.

They are two answers to the same magnetic question.

Tokamaks say:

> use plasma current and symmetry to make helical confinement.

Stellarators say:

> build the helical confinement into external geometry.

One fights current.
The other fights geometry.

Both are trying to make magnetic field lines behave long enough for fusion to become engineering rather than aspiration.
