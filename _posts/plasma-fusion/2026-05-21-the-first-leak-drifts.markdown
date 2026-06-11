---
layout: post
title: "The First Leak: Drifts"
date: 2026-05-21 00:00:00 +0800
categories: plasma fusion conceptual
permalink: /plasma-fusion/drifts/
series: plasma-fusion
series_layer: conceptual
series_order: 4
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/drifts/
description: "E x B drift, grad-B drift, curvature drift, and why magnetic confinement is hard."
excerpt: "E x B drift, grad-B drift, curvature drift, and why magnetic confinement is hard."
---

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/drifts/" | relative_url }}">中文</a></p>

[Back to Plasma & Fusion series]({{ "/plasma-fusion/" | relative_url }})


# The First Leak: Drifts

*E × B drift, grad-B drift, curvature drift, and why magnetic confinement is hard*

In the previous essay, we saw why a magnetic field does not trap particles like a wall.

A wall blocks position.
A magnetic field redirects velocity.

That distinction matters. A charged particle moving across a magnetic field does not simply pass through freely. The Lorentz force bends its path into Larmor motion. The particle circles rapidly around a magnetic field line while also moving along the field. If the perpendicular orbit is small compared with the size of the machine, the particle is said to be strongly magnetized.

At that point, the naive picture becomes tempting:

the particle is no longer flying straight into the wall, so perhaps the plasma is confined.

But this is only the first layer of the story.

A magnetized particle does not just have a position. It has a **guiding center**: the center of its fast circular orbit. The Larmor motion may be tight, but the guiding center itself can move.

This is the first leak.

Magnetic confinement does not first fail because particles ignore the magnetic field. It fails because even particles that obey the magnetic field can slowly drift across it.

---

## 1. From Larmor motion to guiding-center motion

The first picture is simple.

In a uniform magnetic field, a charged particle gyrates. The magnetic force is always perpendicular to the velocity, so it changes the direction of motion but does not change the particle’s kinetic energy. The result is a circular orbit perpendicular to the field, plus free motion along the field.

That gives the basic helical trajectory.

But for confinement, the fast circular motion is not the most important thing. The important question is:

**Where does the center of that circle go?**

If the guiding center remains on a good magnetic surface, the particle is effectively confined. If the guiding center drifts across magnetic surfaces, the particle slowly leaks outward.

So the problem shifts.

We are no longer asking only:

> Does the magnetic field make the particle gyrate?

It does.

We are asking:

> Does the magnetic geometry keep the guiding center from drifting away?

That is a much harder question.

Chen introduces this logic in Chapter 2 through single-particle motion in prescribed electric and magnetic fields, then develops the major guiding-center drifts: electric-field drift, grad-B drift, curvature drift, mirror motion, and adiabatic invariants. 

---

## 2. E × B drift: the whole orbit slides

The cleanest drift appears when an electric field is perpendicular to a magnetic field.

Suppose the magnetic field points one way and the electric field points across it. The particle still gyrates, but the orbit is no longer perfectly symmetric. During one part of the orbit, the electric field accelerates the particle. During another part, it decelerates it.

That means the Larmor radius is slightly larger on one side and slightly smaller on the other.

The circle does not stay centered.

It slides.

The guiding-center velocity is

$$
\mathbf{v}_E = \frac{\mathbf{E}\times \mathbf{B}}{B^2}.
$$

This is the **E × B drift**.

The strange and important thing is that this drift does not depend on the particle’s charge, mass, or speed.

Electrons and ions drift in the same direction at the same velocity.

That makes E × B drift different from many other drifts. It usually does not directly separate charge. Instead, it moves the plasma as a whole, almost like the plasma is being carried sideways by the electromagnetic field.

This is already a warning.

A magnetic field may suppress direct cross-field motion, but if an electric field appears, the entire magnetized plasma can acquire a cross-field drift.

And in a real plasma, electric fields are not exotic. They can arise from pressure gradients, boundary layers, waves, charge separation, turbulence, and the plasma’s own attempt to maintain quasineutrality.

So the first leak is not a particle smashing through the magnetic field.

It is the guiding center quietly sliding sideways.

### 2.4 Nonuniform electric fields: drifts have scale limits

The $E\times B$ drift above assumes that the electric field is almost constant across one Larmor orbit.
That is one of the hidden conditions behind the guiding-center approximation:

$$
r_L \ll L_E,
$$

where $L_E$ is the scale over which the electric field changes appreciably.

If the electric field varies significantly over a single gyration, the particle samples different electric fields at different phases of its orbit. A guiding center can still be useful, but it is no longer determined only by the electric field at one point. The particle responds to a gyroaveraged field.

The physical point is important.

Drift formulas are not magic.
They are approximations built on scale separation.

If fields vary too rapidly over a Larmor radius, the particle is no longer simply gyrating in a local field and drifting slowly. Finite-Larmor-radius effects begin to matter, and the simple guiding-center picture becomes rough.

This is why magnetized plasma always carries an implicit question:

> How large is the structure compared with the Larmor radius?

If the structure is much larger than $r_L$, guiding-center drift is good language.
If it is comparable to $r_L$, the finite width of the particle orbit cannot be ignored.
If it is smaller than $r_L$, the particle does not see it as a smooth background.

This idea returns later in waves, kinetic theory, and turbulent transport. Short-wavelength fluctuations, cyclotron resonance, Bernstein waves, gyroaveraging, and finite-Larmor-radius corrections all remind us that gyration cannot always be erased.

### 2.5 Time-varying electric fields: polarization drift

The $E\times B$ drift has another often hidden assumption:

the electric field must not change too quickly in time.

If the perpendicular electric field $\mathbf{E}_\perp$ changes with time, the $E\times B$ velocity must change too. But particles have inertia. The guiding center cannot adjust instantaneously to the new $E\times B$ velocity without additional dynamics.

That lag produces **polarization drift**.

In the simplest uniform-field, slowly varying approximation, its scale is

$$
\mathbf{v}_p
=
\frac{m}{qB^2}
\frac{d\mathbf{E}_\perp}{dt}.
$$

This differs from $E\times B$ drift in a crucial way: it depends on $m/q$.

So polarization drift is not the same for ions and electrons. Because ions are much heavier, ion polarization drift is often more important. A time-varying electric field can therefore produce a polarization current.

This deepens the drift story.

A static $E\times B$ drift carries ions and electrons together and usually does not directly create current.
A changing $E\times B$ drift requires different species to accelerate differently, so it creates a current response.

This matters for waves and low-frequency plasma dynamics. Many fluctuations, turbulent motions, and edge phenomena contain time-varying electric fields. The plasma is not only carried by $\mathbf{E}\times\mathbf{B}$ motion; it also pays an inertial cost for changing that motion.

Polarization drift is one place where mass has not disappeared from guiding-center theory.

### 2.6 Time-varying magnetic fields: induced fields and betatron intuition

If the magnetic field changes in time, another layer appears.

A changing magnetic field is not just a parameter $B(t)$. Maxwell's equations tell us that a time-varying magnetic field produces a rotational electric field:

$$
\nabla\times\mathbf{E}
=
-\frac{\partial \mathbf{B}}{\partial t}.
$$

The particle therefore feels an induced electric field. That field can do work and change the particle energy.

If the change is slow enough, the fast gyration can still be averaged away. Then an important intuition appears: when the magnetic field slowly increases, the perpendicular energy tends to increase; when the magnetic field slowly decreases, the perpendicular energy tends to fall. This is the betatron acceleration picture.

The deeper structure behind it is the first adiabatic invariant:

$$
\mu = \frac{mv_\perp^2}{2B}.
$$

If $\mu$ is approximately conserved, then an increase in $B$ requires an increase in $v_\perp^2$. The magnetic field does not push along the velocity like an ordinary force, but through the induced electric field and the phase-averaged gyro-orbit, the perpendicular energy still changes.

This shows that drift theory is not a collection of isolated formulas.

It points toward a larger question:

> After fast periodic motion is averaged away, what remains approximately conserved under slow change?

That is the subject of adiabatic invariants.
They explain magnetic mirrors, trapped particles, and why some particle orbits remain ordered for long times in complicated magnetic fields.

So a discussion of drifts should not stop at $E\times B$, grad-$B$, and curvature drift.
It also has to see how spatial variation, temporal variation, and scale separation decide when the guiding-center picture is reliable.

---

## 3. Any transverse force can create a drift

The E × B drift is not a special trick. It is one example of a more general rule.

If a charged particle feels a force $\mathbf{F}$ across the magnetic field, its guiding center drifts as

$$
\mathbf{v}_F = \frac{1}{q}\frac{\mathbf{F}\times \mathbf{B}}{B^2}.
$$

This formula is conceptually important because it says:

a push across the magnetic field does not simply move the particle in the direction of the push.

The particle is already gyrating. A transverse force changes different parts of the orbit differently. The result is not direct motion along the force, but a drift perpendicular to both the force and the magnetic field.

This is one of the basic habits one has to build in plasma physics.

In ordinary mechanics, force points roughly where acceleration happens.

In magnetized plasma motion, force often produces sideways guiding-center drift.

That is why magnetic confinement is so geometric. Every field gradient, every curvature, every pressure force, every electric field has to be interpreted through the geometry of drift.

---

## 4. Grad-B drift: nonuniform magnetic fields separate species

The previous picture assumed the magnetic field was uniform.

A confinement device cannot satisfy that ideal. Magnetic fields are produced by coils. They vary in space. In a torus, the magnetic field is usually stronger on the inner side and weaker on the outer side. Near mirrors, coils, edges, and shaped geometry, the field strength changes.

Once $B$ varies across a particle’s orbit, the Larmor radius varies too:

$$
r_L = \frac{mv_\perp}{|q|B}.
$$

Where the magnetic field is stronger, the Larmor radius is smaller.
Where the magnetic field is weaker, the Larmor radius is larger.

So the orbit becomes asymmetric even without an electric field.

That asymmetry creates **grad-B drift**.

The important point is not just the formula. The important point is the sign.

Grad-B drift depends on charge. Ions and electrons drift in opposite directions.

That changes the story.

E × B drift moves the whole plasma together.
Grad-B drift tends to separate species.

If ions drift one way and electrons drift the other way, the plasma develops currents and charge separation. But a plasma strongly resists large charge separation, because electric fields quickly appear. Those electric fields then produce E × B drift, which can move the plasma as a whole.

So grad-B drift is not merely a single-particle correction. It can trigger a collective response.

This is one of the recurring patterns in plasma physics:

single-particle motion creates charge separation;
charge separation creates fields;
fields move the plasma;
plasma motion changes the fields again.

The leak is already becoming self-consistent.

---

## 5. Curvature drift: closing the field creates a new problem

If magnetic field lines were straight and infinite, particles could stream freely along them and escape from the ends.

So a confinement device needs some way to avoid open-ended loss.

The natural idea is to close the field lines into a torus.

But closing the field creates a new problem: curvature.

A particle moving along a curved magnetic field has parallel velocity whose direction is constantly changing. In the guiding-center picture, this produces an effective centrifugal force away from the center of curvature.

That force produces **curvature drift**.

The curvature drift has the form

$$
\mathbf{v}_R
=
\frac{mv_\parallel^2}{qB^2}
\frac{\mathbf{R}_c \times \mathbf{B}}{R_c^2},
$$

where $\mathbf{R}_c$ is the radius-of-curvature vector of the magnetic field line.

Again, the sign depends on charge. Ions and electrons drift in opposite directions.

This is where magnetic confinement becomes beautifully cruel.

Open magnetic fields leak along the ends.

Closed magnetic fields avoid end loss, but the act of bending the field introduces curvature drift.

So the torus is not automatically a solution. It is a trade.

You remove one leak and create another.

---

## 6. The simple torus fails

Now we can see why a simple toroidal magnetic field is not enough.

Imagine taking a straight magnetic field and bending it into a doughnut. The field lines close, so particles no longer simply stream out of the ends. That sounds like progress.

But in a torus, the magnetic field is not uniform. The inner side of the torus has stronger magnetic field; the outer side has weaker magnetic field. So grad-B drift appears.

The field lines are also curved. So curvature drift appears.

Worse, in a simple toroidal field, these two drifts tend to add rather than cancel.

The result is species separation. Ions drift one way, electrons drift the other way. This charge separation produces an electric field. That electric field produces an E × B drift. The E × B drift can push the whole plasma outward.

This is the first major geometric failure of naive magnetic confinement.

The plasma is not lost because the particles were unmagnetized.

They are lost because the magnetic field is curved and nonuniform in a way that gives their guiding centers a systematic sideways drift.

Chen makes this point sharply in the discussion of curved magnetic fields: if one bends a magnetic field into a torus to confine a thermonuclear plasma, the resulting drift tends to carry particles out unless the magnetic geometry is modified. 

That is the key transition.

The problem is no longer:

> Can a magnetic field make charged particles gyrate?

Yes.

The problem is:

> Can a closed magnetic field be designed so that the unavoidable drifts average out?

That question leads directly to tokamaks and stellarators.

---

## 7. Tokamaks and stellarators are drift-management machines

A tokamak is not just a torus with a strong magnetic field.

It is a torus with twisted magnetic field lines.

The field has a strong toroidal component around the main direction of the doughnut, plus a poloidal component around the minor cross-section. Together, they create helical field lines.

This twist matters because particles no longer remain permanently on one bad side of the torus. As they follow the helical field, they sample different regions: inner side, outer side, top, bottom, stronger field, weaker field, good curvature, bad curvature.

The goal is not to eliminate drift locally. That is impossible.

The goal is to arrange the geometry so that drifts average out over time.

A stellarator takes this idea even further.

Instead of relying mainly on a large plasma current to help twist the field, a stellarator builds the twist into the external magnetic geometry itself. Its coils are complex because the problem is complex: the device is trying to sculpt a three-dimensional magnetic field in which guiding-center orbits remain confined.

From the drift point of view, a stellarator is not strange because engineers enjoy strange coils.

It is strange because the machine is trying to solve a strange problem:

> Design a magnetic field that is closed, curved, nonuniform, three-dimensional — and yet does not let particle drifts accumulate into radial loss.

That is a brutal geometric constraint.

And it is why stellarator optimization is so hard. The task is not merely to produce a strong magnetic field. It is to produce a magnetic field whose imperfections compensate each other in phase space.

---

## 8. Drifts are not small corrections

It is tempting to treat drifts as secondary effects.

First, we learn the clean picture: charged particles spiral around magnetic field lines.

Then we add small corrections: E × B drift, grad-B drift, curvature drift.

But for magnetic confinement, these “corrections” are the problem.

A fusion plasma must be extremely hot. At such temperatures, particles move fast. Fast particles drift. Hot plasmas also have pressure gradients. Pressure gradients create currents. Currents modify magnetic fields. Modified magnetic fields change particle orbits. Particle orbits change transport.

So confinement is not a static cage problem.

It is a self-consistent dynamical problem.

Particles move in fields, but the particles also create fields.
Fields guide particles, but particle motion also changes the fields.
Geometry controls drift, but drift also determines whether the geometry works.

The guiding-center approximation is powerful because it simplifies the fast Larmor motion. But it also reveals the deeper difficulty: once the fast circle is averaged away, the slow drift remains.

And slow is enough.

Fusion does not require particles to escape instantly. It only takes a persistent sideways leak to drain energy and particles faster than the plasma can sustain burning.

---

## 9. The first leak

The previous essay ended with a basic correction:

a magnetic field is not a wall.

This essay adds the next correction:

even when the magnetic field works, confinement can still fail.

The field magnetizes the particles.
The particles gyrate.
The guiding centers emerge.
Then the guiding centers drift.

E × B drift shows that the whole plasma can slide across the field.
Grad-B drift shows that nonuniform field strength separates species.
Curvature drift shows that closing field lines into a torus creates centrifugal drift.
The simple torus fails because these drifts become systematic.
Tokamaks and stellarators exist because the geometry must be twisted, shaped, and optimized so that drifts do not add up to loss.

So the first leak in magnetic confinement is not dramatic.

It is not a particle punching through a magnetic wall.

It is slower and subtler:

the center of the orbit moves.

That is enough to make fusion hard.
