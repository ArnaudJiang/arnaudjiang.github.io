---
layout: post
title: "Plasma & Fusion"
date: 2026-05-19 09:00:00 +0800
categories: plasma fusion physics
permalink: /plasma-fusion/
---

This is the starting point for my notes on plasma physics and nuclear fusion.

I studied physics, but I am approaching this topic again from a new position: with more engineering experience, more exposure to AI systems, and a stronger interest in simulation, computation, and applied scientific infrastructure. Plasma and fusion sit at an unusual intersection of theory, experiment, control, materials, numerical methods, and large-scale engineering. That makes the field difficult, but also unusually rich.

This series will be a public notebook for rebuilding my understanding step by step.

## What I Want To Understand

The first goal is to rebuild the conceptual foundation:

- What plasma is, and why collective behavior matters
- How charged particles move in electromagnetic fields
- Why confinement is hard
- What makes fusion physically possible but technologically difficult
- How tokamaks, stellarators, inertial confinement, and alternative concepts differ
- Which equations and approximations are actually used in practice

The second goal is computational:

- Magnetohydrodynamics and kinetic descriptions
- Particle-in-cell methods
- Numerical stability and discretization choices
- Simulation workflows for plasma systems
- The role of AI in surrogate modeling, control, diagnostics, and experiment planning

The third goal is to connect physics with real engineering:

- Materials under neutron flux
- Heating, current drive, and plasma control
- Diagnostics and data pipelines
- Reactor design constraints
- The economics and timelines of fusion technology

## How I Plan To Write

These posts will not be polished lecture notes at the beginning. I expect them to look more like working notes: definitions, diagrams, derivations, implementation experiments, paper summaries, and occasional corrections to my own earlier understanding.

I want the writing to stay close to the process of learning. Some posts may explain a single equation. Others may review a paper, reproduce a simple simulation, or compare different confinement approaches. Over time, I hope this becomes a small map of the field from the perspective of someone moving between physics, AI, and software engineering.

## Initial Questions

The questions I want to start with are:

- What is the minimum mathematical toolkit needed to reason about plasma behavior?
- When is MHD enough, and when do kinetic effects become unavoidable?
- What are the core failure modes of magnetic confinement?
- Which parts of fusion research are most constrained by physics, and which are constrained by engineering?
- Where can modern AI tools help without hiding the underlying science?

This post is only the marker on the map. The actual work begins with the fundamentals.
