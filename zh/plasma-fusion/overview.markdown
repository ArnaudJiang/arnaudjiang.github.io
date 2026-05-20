---
layout: page
title: "Plasma & Fusion：概览"
permalink: /zh/plasma-fusion/overview/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/overview/
series: plasma-fusion
series_layer: origin
series_order: 0
description: "从带电物质的集体行为出发，经由计算模型，走向磁约束聚变与仿星器设计。"
---

这是我关于等离子体物理与核聚变笔记的起点。

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/overview/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

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

## 我打算怎么写

这些文章一开始不会是完全打磨好的讲义。它们更像工作笔记：定义、图示、推导、实现实验、论文总结，以及对自己早期理解的修正。

我希望写作尽量贴近学习过程。有些文章可能只解释一个方程；有些文章可能会读一篇论文、复现一个简单仿真，或者比较不同的约束思路。随着时间推进，我希望它能成为一张小型地图：从一个在物理、AI 和软件工程之间移动的视角，重新理解这个领域。

[系列页]({{ "/zh/plasma-fusion/" | relative_url }})是地图。真正的工作从基本概念开始。
