---
layout: post
title: "Adiabatic Invariants: Hidden Constraints in Particle Orbits"
date: 2026-05-21 01:00:00 +0800
categories: plasma fusion conceptual
permalink: /plasma-fusion/adiabatic-invariants/
series: plasma-fusion
series_layer: conceptual
series_order: 5
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/adiabatic-invariants/
description: "Magnetic moment, bounce invariant, flux invariant, and why they matter for mirrors, trapped particles, and confinement."
excerpt: "Magnetic moment, bounce invariant, flux invariant, and why they matter for mirrors, trapped particles, and confinement."
---

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/adiabatic-invariants/" | relative_url }}">中文</a></p>

[Back to Plasma & Fusion series]({{ "/plasma-fusion/" | relative_url }})

# Adiabatic Invariants: Hidden Constraints in Particle Orbits

*Magnetic moment, bounce invariant, flux invariant, and why they matter for mirrors, trapped particles, and confinement*

The previous essays built a picture:

a magnetic field does not trap particles like a wall.
It makes charged particles gyrate.
The center of that gyration can drift.

But single-particle motion has another layer.

In slowly varying magnetic fields, particle motion is not arbitrary. Even when an orbit looks complicated, certain combinations of quantities remain approximately conserved. These are **adiabatic invariants**.

Here, adiabatic does not mean the thermodynamic idea of no heat exchange.

It means:

> the external conditions change slowly compared with a fast periodic motion, so a cycle-averaged quantity remains nearly conserved.

That idea is powerful.

It says that a particle is not only controlled by the instantaneous force. It is also constrained by the periodic structure of its own motion.

---

## 1. Why adiabatic invariants appear

A charged particle in a magnetic field gyrates rapidly.

The gyrofrequency is

$$
\Omega_c = \frac{|q|B}{m}.
$$

If the magnetic field changes very little during one gyration, the particle sees an almost steady environment. It completes many orbits before the background changes appreciably.

That separation of scales is the key:

$$
\frac{1}{\Omega_c} \ll \tau_B,
$$

where $\tau_B$ is the time scale on which the particle sees the magnetic field change.

When fast motion and slow variation are separated, the fast phase can be averaged away. After that averaging, action-like quantities can become approximately conserved.

For magnetized particles, the three main adiabatic invariants correspond to three progressively slower periodic motions:

1. gyration;
2. bounce motion;
3. drift motion.

---

## 2. The first invariant: magnetic moment

The first adiabatic invariant is the **magnetic moment**:

$$
\mu = \frac{mv_\perp^2}{2B}.
$$

Here $v_\perp$ is the particle velocity perpendicular to the magnetic field.

The intuition is simple: a gyrating charged particle behaves like a tiny current loop. A current loop has a magnetic moment. If the field changes slowly and smoothly enough, that magnetic moment is nearly conserved.

If a particle moves into a stronger magnetic field, $B$ increases. To keep $\mu$ constant, $v_\perp^2$ must increase.

The perpendicular energy rises.

If there is no electric field doing net work, the total kinetic energy remains nearly constant. The parallel energy must therefore fall:

$$
\frac{1}{2}mv^2
=
\frac{1}{2}mv_\perp^2
+
\frac{1}{2}mv_\parallel^2.
$$

This is the core of magnetic mirror motion.

A strong magnetic field does not reflect the particle like a hard wall. It converts parallel kinetic energy into perpendicular kinetic energy through magnetic-moment conservation. When $v_\parallel$ reaches zero, the particle reverses direction.

---

## 3. Mirror motion: reflection from a conserved quantity

Suppose a particle moves from a weak-field region into a strong-field region.

If $\mu$ is conserved,

$$
\frac{mv_\perp^2}{2B}
=
\text{constant}.
$$

As $B$ increases, $v_\perp^2$ increases.

If total energy is conserved, $v_\parallel^2$ decreases.

At some point, one may have

$$
v_\parallel = 0.
$$

That point is the mirror point.

Conceptually, the mirror force pushes the particle back toward weaker field along the magnetic field line. It can be written approximately as

$$
F_\parallel = -\mu \nabla_\parallel B.
$$

The particle is not bouncing off a material object. It responds to the variation of magnetic-field strength along the field line.

Strong-field regions repel particles with enough perpendicular energy.

This explains why magnetic mirrors can confine some particles and why they cannot confine all particles.

Particles with too much parallel velocity and too little perpendicular velocity fall into the loss cone and escape.

---

## 4. The loss cone is velocity-space structure

Use the pitch angle $\alpha$ to describe the direction of velocity:

$$
\sin^2\alpha = \frac{v_\perp^2}{v^2}.
$$

If the starting field is $B_0$ and the mirror field is $B_m$, the rough reflection condition is

$$
\sin^2\alpha_0 \ge \frac{B_0}{B_m}.
$$

Particles with large enough perpendicular velocity are reflected.

Particles with too much parallel velocity are lost.

This gives an important lesson:

> magnetic geometry does not only constrain space; it also selects velocity space.

Two particles starting from the same position can have different fates if their pitch angles differ.

That is one reason kinetic theory becomes unavoidable. A fluid variable may tell us density and temperature, but a loss cone is structure in velocity space.

---

## 5. The second invariant: bounce action

If a particle is trapped between two mirror points, it bounces along the field line.

This bounce motion is slower than Larmor gyration, but it can still be periodic.

When the magnetic structure changes slowly compared with the bounce period, the second adiabatic invariant appears:

$$
J = \oint mv_\parallel\, ds.
$$

The integral is taken over one complete bounce motion between mirror points.

The first invariant constrains gyration.
The second constrains bounce motion.

This matters for trapped particles.

In tokamaks and stellarators, the magnetic-field strength varies along a field line. Some particles are trapped by magnetic mirrors in low-field regions instead of freely passing around the torus.

These trapped particles drift, collide, and transport differently from passing particles.

So adiabatic invariants are not mathematical decoration. They determine particle populations.

---

## 6. The third invariant: flux enclosed by drift motion

The third adiabatic invariant corresponds to an even slower drift motion.

If the guiding center slowly drifts around a closed region, and if the magnetic field changes slowly compared with that drift period, the magnetic flux enclosed by the drift orbit is approximately conserved.

A common way to express the idea is

$$
\Phi = \oint \mathbf{A}\cdot d\mathbf{l}.
$$

This invariant is usually more fragile than the first two.

That is because it depends on the largest spatial scale and slowest period. In a real confinement device, collisions, turbulence, ripple, islands, stochastic field lines, and time-dependent perturbations can all break it.

But the concept is still useful.

It connects particle motion to magnetic flux surfaces. If the flux enclosed by the drift orbit is conserved, the particle is more likely to remain near the same class of magnetic surface. If that constraint is broken, radial transport grows.

---

## 7. When the invariants fail

Adiabatic invariants are approximations, not contracts.

They require:

1. fields that change little during one period;
2. spatial scales larger than the relevant orbit size;
3. weak enough collisions and perturbations;
4. no strong resonance or separatrix crossing that destroys the periodic motion.

The first invariant requires smooth fields over a Larmor radius.
The second requires well-defined bounce motion.
The third requires sufficiently coherent drift orbits.

When these conditions fail, the invariants are broken.

That is why edges, strong turbulence, magnetic islands, stochastic field lines, wave-particle resonances, and collisions matter so much. They can destroy the slow conserved structure of the orbit.

Once that structure is broken, particles diffuse more easily through phase space.

Confinement degrades.

---

## 8. Why this matters especially for stellarators

A stellarator is a three-dimensional magnetic geometry machine.

Its goal is not merely to make a strong magnetic field. It is to make a magnetic field that is good in phase space.

That means caring about trapped particles, drift orbits, bounce motion, and neoclassical transport.

Adiabatic invariants are the language that connects those topics.

The first invariant tells us how particles exchange parallel and perpendicular energy in varying magnetic fields.
The second tells us how trapped-particle bounce motion remains structured.
The third tells us whether drift orbits remain tied to magnetic flux surfaces.

If the geometry is poor, trapped-particle drifts can move particles radially outward.
If the geometry is well optimized, those offsets can average away over bounce or drift motion.

That is one motivation behind quasisymmetry, omnigeneity, and stellarator optimization:

> design the magnetic field so that the adiabatic orbit structure does not send particles to the wall.

---

## 9. Conceptual conclusion

Drifts tell us that guiding centers move.

Adiabatic invariants tell us that this motion is not completely arbitrary.

Particles have fast gyration, slower bounce motion, and even slower drift motion. Each periodic layer can leave behind an approximately conserved quantity if the background changes slowly and smoothly enough.

Those conserved quantities make magnetic confinement possible.

They also reveal its fragility.

If $\mu$ is conserved, a magnetic mirror can reflect particles.
If $J$ is conserved, trapped-particle motion has predictable structure.
If drift flux is approximately conserved, particles are more likely to remain near good magnetic surfaces.

But if collisions, turbulence, resonances, or three-dimensional imperfections break these invariants, particles diffuse through phase space, transport increases, and confinement worsens.

Adiabatic invariants are therefore not an appendix.

They are a key bridge from single-particle orbits to magnetic confinement:

magnetic fields do not only bend particles.
They also create approximate conserved structures in particle motion.

The difficulty of fusion is keeping those structures reliable in a real, hot, weakly collisional, three-dimensional, self-consistent plasma.
