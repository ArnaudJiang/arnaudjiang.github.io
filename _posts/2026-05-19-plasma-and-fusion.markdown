---
layout: post
title: "Plasma & Fusion"
date: 2026-05-19 09:00:00 +0800
categories: plasma fusion physics
permalink: /plasma-fusion/
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/
description: "A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design."
excerpt: "This is the starting point for my notes on plasma physics and nuclear fusion."
---

This is the starting point for my notes on plasma physics and nuclear fusion.

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/" | relative_url }}">中文</a></p>

I studied physics, but I am approaching this topic again from a new position: with more engineering experience, more exposure to AI systems, and a stronger interest in simulation, computation, and applied scientific infrastructure. Plasma and fusion sit at an unusual intersection of theory, experiment, control, materials, numerical methods, and large-scale engineering. That makes the field difficult, but also unusually rich.

This series will be a public notebook for rebuilding my understanding step by step.

> A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design.

## Origin: Why Plasma & Fusion

This entry is not meant to be a tutorial opening. It is a research motivation statement.

I want to understand why plasma is such a difficult object to control, why fusion turns that difficulty into an engineering problem at planetary scale, and how computation, simulation, and AI may help without hiding the underlying physics.

The series will use Francis F. Chen's *Introduction to Plasma Physics and Controlled Fusion* as one of the main references, but it will not be organized as chapter-by-chapter reading notes. I want it to become a knowledge map that moves from physics intuition, to modeling choices, to magnetic fusion and stellarator thinking.

## Series Structure

The series has three layers. They are not simply "easy, medium, hard." They are organized by cognitive scale.

| Layer | Main task | Writing style | Formula density |
| --- | --- | --- | --- |
| Origin | Explain the motivation | Personal research note | Very low |
| Conceptual | Build physical intuition | Images, analogies, simple diagrams | Low |
| Modeling | Build the model stack | Approximation, tradeoff, equation meaning | Medium |
| Fusion / Stellarator | Connect physics to devices | Physics to device to engineering | Medium-low |

Future posts in this series will stay under the same URL prefix:

```text
/plasma-fusion/plasma-is-not-gas/
/plasma-fusion/magnetic-fields/
/plasma-fusion/modeling-stack/
/plasma-fusion/stellarator-geometry/
```

The source files will remain ordinary Markdown posts in `_posts/`. Each post only needs a stable `permalink`:

```markdown
---
layout: post
title: "Plasma Is Not Just Ionized Gas"
date: 2026-05-20 09:00:00 +0800
categories: plasma fusion conceptual
permalink: /plasma-fusion/plasma-is-not-gas/
---
```

## I. Conceptual Layer: What Is Plasma?

This layer builds an intuition map for the first half of Chen's book. The main question is:

> Why is plasma not just ordinary ionized gas?

The goal is to understand why collective behavior matters, why magnetic fields can constrain charged particles, and why confinement is never as clean as the first picture suggests.

Planned posts:

1. **Plasma Is Not Just Ionized Gas**  
   Debye shielding, quasineutrality, and collective behavior.

2. **Magnetic Fields Do Not Trap Particles Like Walls**  
   Larmor motion, guiding centers, and why magnetic fields mostly restrict transverse motion.

3. **The First Leak: Drifts**  
   E x B drift, grad-B drift, curvature drift, and why magnetic confinement is hard.

4. **From Particles to Fluids**  
   Why plasma can sometimes be treated as a fluid, and where that approximation begins to break.

5. **Waves Are the Language of Plasma**  
   Plasma oscillations, Alfven waves, cutoff, resonance, and wave-particle intuition.

Target reader: someone who does not know plasma physics yet, but wants to know why it is worth learning.

## II. Modeling Layer: How Do We Describe Plasma?

This layer moves from intuition to the model stack. The main question is:

> What does each plasma model preserve, and what does it throw away?

The point is not to derive every equation from first principles. The point is to understand why different descriptions exist, when each one is useful, and what kinds of questions each model can or cannot answer.

The model stack looks roughly like this:

```text
Single-particle model
↓
Fluid model
↓
MHD model
↓
Kinetic model
↓
Nonlinear effects, turbulence, and simulation
```

Planned posts:

1. **The Plasma Modeling Stack**  
   A map of particle, fluid, MHD, kinetic, and PIC descriptions.

2. **Fluid Plasma: The First Useful Approximation**  
   Continuity, momentum, pressure, and self-consistent fields.

3. **MHD: When Plasma Becomes a Conducting Fluid**  
   Why fusion devices care so much about equilibrium and stability.

4. **Diffusion and Transport: Why Confinement Is a Time-scale Problem**  
   Classical diffusion, neoclassical diffusion, and Bohm diffusion as physical ideas.

5. **Kinetic Theory: When Averages Are Not Enough**  
   Distribution functions, Landau damping, and wave-particle interaction.

6. **Nonlinearity and Turbulence: Where Simple Models Break**  
   Instability growth, transport, and why confinement is often controlled by turbulence.

Target reader: someone with some math or engineering background who wants to understand how plasma physics is modeled and computed.

## III. Fusion / Stellarator Layer: How Does This Become a Device?

This layer connects plasma physics to magnetic confinement fusion, especially stellarators. The main question is:

> If the final goal is fusion, what job does each earlier concept actually do?

The storyline is:

```text
Fusion needs high temperature
↓
High temperature means plasma
↓
Plasma must be confined
↓
Magnetic fields can confine charged particles
↓
Toroidal magnetic fields create drifts
↓
Drifts cause losses
↓
Stellarators use 3D magnetic geometry to control those losses
```

Planned posts:

1. **Why Fusion Is a Confinement Problem**  
   Temperature, density, and energy confinement time before device details.

2. **Magnetic Confinement: The Promise and the Trap**  
   Why magnetic fields help, and why toroidal geometry creates drift losses.

3. **Tokamak vs Stellarator: Two Ways to Twist Magnetic Fields**  
   Not a catalog comparison, but a question of how to make field lines behave.

4. **Why Stellarators Are Geometry Machines**  
   Rotational transform, magnetic surfaces, 3D coils, and quasisymmetry.

5. **The Stellarator Transport Problem**  
   Drifts, magnetic mirrors, adiabatic invariants, and neoclassical transport.

6. **From Plasma Physics to Fusion Engineering**  
   Heating, diagnostics, materials, control, simulation, and AI interfaces.

Target reader: someone who wants to move from plasma basics toward magnetic confinement fusion and stellarator design.

## How I Plan To Write

These posts will not be polished lecture notes at the beginning. I expect them to look more like working notes: definitions, diagrams, derivations, implementation experiments, paper summaries, and occasional corrections to my own earlier understanding.

I want the writing to stay close to the process of learning. Some posts may explain a single equation. Others may review a paper, reproduce a simple simulation, or compare different confinement approaches. Over time, I hope this becomes a small map of the field from the perspective of someone moving between physics, AI, and software engineering.

This page is the map. The actual work begins with the fundamentals.
