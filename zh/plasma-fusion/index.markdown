---
layout: page
title: "Plasma & Fusion"
permalink: /zh/plasma-fusion/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/
description: "从带电物质的集体行为出发，经由计算模型，走向磁约束聚变与仿星器设计。"
---

这是我关于等离子体物理与核聚变笔记的起点。

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/" | relative_url }}">English</a> | 中文</p>

我学过物理，但这一次重新进入这个主题时，位置已经不同：我有了更多工程经验，对 AI 系统也有了更多接触，同时更关注仿真、计算和应用科学基础设施。等离子体与聚变位于理论、实验、控制、材料、数值方法和大型工程的交叉点上。它很难，也因此非常丰富。

这个系列会是一个公开笔记本，用来一步一步重建我的理解。

> 从带电物质的集体行为出发，经由计算模型，走向磁约束聚变与仿星器设计。

## Origin：为什么关注 Plasma & Fusion

这篇文章不是教程开篇，而是一份研究动机声明。

[阅读独立的 Origin 笔记。]({{ "/zh/plasma-fusion/origin/" | relative_url }}) / [English]({{ "/plasma-fusion/origin/" | relative_url }})

我想理解：为什么等离子体是如此难以控制的对象；为什么聚变会把这种困难放大成行星尺度的工程问题；以及计算、仿真和 AI 如何在不遮蔽底层物理的前提下参与其中。

这个系列会以 Francis F. Chen 的 *Introduction to Plasma Physics and Controlled Fusion* 作为主要参考之一，但它不会写成逐章读书笔记。我更希望它成为一张知识地图：从物理直觉，到建模选择，再到磁约束聚变与仿星器思维。

## 系列结构

这个系列分成三层。它们不是简单的“浅、中、深”，而是按照认知尺度来组织。

| 层级 | 主要任务 | 写作风格 | 公式密度 |
| --- | --- | --- | --- |
| Origin | 解释动机 | 个人研究笔记 | 很低 |
| Conceptual | 建立物理直觉 | 图像、类比、简图 | 低 |
| Modeling | 建立模型栈 | 近似、取舍、方程含义 | 中 |
| Fusion / Stellarator | 连接物理与装置 | 从物理到装置再到工程 | 中低 |

后续文章会统一放在同一个 URL 前缀下：

```text
/plasma-fusion/plasma-is-not-gas/
/plasma-fusion/magnetic-fields/
/plasma-fusion/modeling-stack/
/plasma-fusion/stellarator-geometry/
```

源文件仍然是 `_posts/` 中的普通 Markdown 文章。每篇文章只需要设置稳定的 `permalink`：

```markdown
---
layout: post
title: "Plasma Is Not Just Ionized Gas"
date: 2026-05-20 09:00:00 +0800
categories: plasma fusion conceptual
permalink: /plasma-fusion/plasma-is-not-gas/
---
```

## I. Conceptual Layer：等离子体到底是什么？

这一层为 Chen 书的前半部分建立一张直觉地图。核心问题是：

> 为什么 plasma 不只是普通的电离气体？

目标是理解为什么集体行为重要，为什么磁场能够约束带电粒子，以及为什么这种约束从一开始就没有想象中那么干净。

计划文章：

1. **Plasma Is Not Just Ionized Gas**  
   Debye shielding、准中性和集体行为。

2. **Magnetic Fields Do Not Trap Particles Like Walls**  
   Larmor motion、guiding center，以及为什么磁场主要限制横向运动。

3. **The First Leak: Drifts**  
   E x B drift、grad-B drift、curvature drift，以及为什么磁约束很难。

4. **From Particles to Fluids**  
   为什么 plasma 有时可以被当作流体，以及这个近似从哪里开始失效。

5. **Waves Are the Language of Plasma**  
   plasma oscillation、Alfven wave、cutoff、resonance 和波粒相互作用直觉。

目标读者：还不了解等离子体物理，但想知道它为什么值得学习的人。

## II. Modeling Layer：我们如何描述等离子体？

这一层从直觉进入模型栈。核心问题是：

> 每一种 plasma 模型保留了什么，又丢掉了什么？

重点不是从第一性原理推导所有方程，而是理解为什么会有不同描述、每种描述什么时候有用，以及它们能回答和不能回答什么问题。

模型栈大致如下：

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

计划文章：

1. **The Plasma Modeling Stack**  
   particle、fluid、MHD、kinetic 和 PIC 描述的地图。

2. **Fluid Plasma: The First Useful Approximation**  
   continuity、momentum、pressure 和自洽场。

3. **MHD: When Plasma Becomes a Conducting Fluid**  
   为什么聚变装置如此关心平衡和稳定性。

4. **Diffusion and Transport: Why Confinement Is a Time-scale Problem**  
   classical diffusion、neoclassical diffusion 和 Bohm diffusion 的物理图像。

5. **Kinetic Theory: When Averages Are Not Enough**  
   分布函数、Landau damping 和波粒相互作用。

6. **Nonlinearity and Turbulence: Where Simple Models Break**  
   不稳定性增长、输运，以及为什么约束常常由湍流控制。

目标读者：有一定数学或工程背景，想理解等离子体物理如何建模和计算的人。

## III. Fusion / Stellarator Layer：这些知识如何变成装置？

这一层把等离子体物理连接到磁约束聚变，尤其是仿星器。核心问题是：

> 如果最终目标是聚变，前面的每个概念到底在服务什么？

主线是：

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

计划文章：

1. **Why Fusion Is a Confinement Problem**  
   先讲温度、密度和能量约束时间，再进入装置细节。

2. **Magnetic Confinement: The Promise and the Trap**  
   为什么磁场有用，以及为什么环形几何会产生漂移损失。

3. **Tokamak vs Stellarator: Two Ways to Twist Magnetic Fields**  
   不做百科式对比，而是围绕“如何让磁力线表现得足够好”来讲。

4. **Why Stellarators Are Geometry Machines**  
   rotational transform、magnetic surfaces、3D coils 和 quasisymmetry。

5. **The Stellarator Transport Problem**  
   drift、magnetic mirror、adiabatic invariant 和 neoclassical transport。

6. **From Plasma Physics to Fusion Engineering**  
   heating、diagnostics、materials、control、simulation 和 AI 的接口。

目标读者：想从等离子体基础走向磁约束聚变，尤其是仿星器设计的人。

## 我打算怎么写

这些文章一开始不会是完全打磨好的讲义。它们更像工作笔记：定义、图示、推导、实现实验、论文总结，以及对自己早期理解的修正。

我希望写作尽量贴近学习过程。有些文章可能只解释一个方程；有些文章可能会读一篇论文、复现一个简单仿真，或者比较不同的约束思路。随着时间推进，我希望它能成为一张小型地图：从一个在物理、AI 和软件工程之间移动的视角，重新理解这个领域。

这一页是地图。真正的工作从基本概念开始。
