---
layout: post
title: "Plasma & Fusion: Overview"
date: 2026-05-19 09:00:00 +0800
categories: plasma fusion physics
permalink: /plasma-fusion/overview/
series: plasma-fusion
series_layer: origin
series_order: 0
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/overview/
description: "A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design."
excerpt: "This is the starting point for my notes on plasma physics and nuclear fusion."
---

This is the starting point for my notes on plasma physics and nuclear fusion.

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/overview/" | relative_url }}">中文</a></p>

[Back to Plasma & Fusion series]({{ "/plasma-fusion/" | relative_url }})

I studied physics, but I am approaching this topic again from a new position: with more engineering experience, more exposure to AI systems, and a stronger interest in simulation, computation, and applied scientific infrastructure. Plasma and fusion sit at an unusual intersection of theory, experiment, control, materials, numerical methods, and large-scale engineering. That makes the field difficult, but also unusually rich.

This series will be a public notebook for rebuilding my understanding step by step.

> A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design.

## Origin: Why Plasma & Fusion

This entry is not meant to be a tutorial opening. It is a research motivation statement.

[Read the standalone Origin note.]({{ "/plasma-fusion/origin/" | relative_url }}) / [中文]({{ "/zh/plasma-fusion/origin/" | relative_url }})

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

The source files will remain ordinary Markdown posts in `_posts/plasma-fusion/`. Each post only needs a stable `permalink`:

```markdown
---
layout: post
title: "Plasma Is Not Just Ionized Gas"
date: 2026-05-20 09:00:00 +0800
categories: plasma fusion conceptual
series: plasma-fusion
series_layer: conceptual
series_order: 2
permalink: /plasma-fusion/plasma-is-not-gas/
---
```

## How I Plan To Write

These posts will not be polished lecture notes at the beginning. I expect them to look more like working notes: definitions, diagrams, derivations, implementation experiments, paper summaries, and occasional corrections to my own earlier understanding.

I want the writing to stay close to the process of learning. Some posts may explain a single equation. Others may review a paper, reproduce a simple simulation, or compare different confinement approaches. Over time, I hope this becomes a small map of the field from the perspective of someone moving between physics, AI, and software engineering.

The [series page]({{ "/plasma-fusion/" | relative_url }}) is the map. The actual work begins with the fundamentals.
