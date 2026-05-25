---
layout: page
title: "Tokamak vs Stellarator：两种扭转磁场的方式"
permalink: /zh/plasma-fusion/tokamak-vs-stellarator/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/tokamak-vs-stellarator/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 14
description: "不做百科式对比，而是围绕“如何让磁力线表现得足够好”来讲。"
excerpt: "不做百科式对比，而是围绕“如何让磁力线表现得足够好”来讲。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/tokamak-vs-stellarator/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Tokamak vs Stellarator：两种扭转磁场的方式

*不做百科式对比，而是围绕“如何让磁力线表现得足够好”来讲*

Tokamak 和 stellarator 常被作为两类 reactor concept 比较。

这有用，但可能遮住更深的问题。

两者都在试图解决同一个 geometry problem：

> 如何让 magnetic field lines 以能够约束 plasma 的方式绕 torus 缠绕？

差别不只是形状。

差别是 twist 从哪里来。

---

## 1. 为什么 field lines 需要 twist

纯 toroidal magnetic field 不够。

粒子会经历 curvature 和 grad-$B$ drifts。没有补偿几何时，这些 drifts 会造成 charge separation 和 outward motion。

Field lines 需要 poloidal motion，也需要 toroidal motion。它们必须 helically 绕 torus，让不同区域被采样，使 drifts 可以平均掉。

这种 helical winding 是共同目标。

Tokamak 和 stellarator 的差别，是它们如何创造它。

---

## 2. Tokamak：让 plasma 携带 twist

Tokamak 用外部 coils 产生强 toroidal field，并用大型 plasma current 产生 poloidal field。

两者合成 helical magnetic field lines。

Tokamak 的美在于 symmetry。

装置近似 axisymmetric。这种 symmetry 有助于 confinement，简化 equilibrium，并提供强大的理论和计算工具。

但 plasma current 既有用，也危险。

它创造所需 twist。
它也创造 current-driven instabilities、disruptions，以及 pulsed-operation 挑战，除非使用 non-inductive current drive。

Tokamak 的交易是：

> geometry 更简单，但 plasma current problem 更中心。

---

## 3. Stellarator：把 twist 做进 coils

Stellarator 试图主要用外部三维 coils 创造所需 helical field。

Plasma 不需要携带大型 toroidal current 来形成基本 confinement geometry。

这给 stellarators 一个重要概念优势：

steady-state operation 更自然，某些 current-driven disruption risks 可以降低。

但代价是 geometry。

Coils 很复杂。Magnetic field 是三维的。Equilibrium、transport 和 optimization 都更难。

Stellarator 的交易是：

> 更少依赖 plasma current，但 geometry problem 难得多。

---

## 4. Axisymmetry 与三维设计

Tokamak axisymmetry 很强大。

它给出 conserved canonical momentum，有助于 particle confinement。它降低 equilibrium 难度。它让 diagnostics、modeling 和 engineering 更规则。

Stellarator 放弃 axisymmetry。

这听起来是损失，也确实是。但精心设计的 3D field 仍然可以在正确坐标中近似有用 symmetry。这就是 quasisymmetry 等思想出现的地方。

Stellarator 不问：

> 能不能让 machine 保持简单？

它问：

> 能不能在复杂 magnetic field 中设计出足够多 hidden order？

---

## 5. Stability 和 disruptions

Tokamaks 可以达到优秀 confinement，但大型 plasma current 带来 disruption risk。Disruption 是 confinement 和 current 的快速丢失，会产生巨大 mechanical 和 thermal loads。

这是 tokamak engineering 的中心挑战之一。

Stellarators 通过减少对大型 plasma current 的依赖，可以避开某些 disruption mechanisms。但这不意味着它们自动稳定。它们仍然面对 pressure-driven modes、islands、neoclassical transport、turbulence 和 edge issues。

对比不是：

> tokamaks 不稳定，stellarators 稳定。

而是：

> tokamaks 和 stellarators 暴露不同 stability problems。

---

## 6. Transport tradeoffs

Tokamaks 受益于 symmetry，但 turbulent transport 仍然是主要问题。

Stellarators 历史上受 neoclassical transport 困扰，因为 3D fields 中的 trapped particles 可能径向 drift。现代 stellarators 通过 optimization 降低这种损失。

这就是 stellarator story 随 computation 改变的原因。

旧 stellarator 是巧妙 magnetic idea。
现代 stellarator 是 numerical design object。

它的 geometry 不只是为了让 field lines 漂亮闭合，而是为了减少 particle losses、改善 MHD behavior、管理 islands，并满足 coil constraints。

---

## 7. Engineering personality

Tokamaks 把困难集中在 plasma control、current drive、disruption avoidance 和 exhaust。

Stellarators 把困难转移到 coil geometry、manufacturing tolerances、3D optimization 和 configuration design。

两者仍然都面对 materials、tritium breeding、heating、diagnostics、maintenance 和 economics。

所以问题不是哪个 concept 容易。

都不容易。

问题是：

> 我们希望困难住在哪里？

---

## 结尾

Tokamaks 和 stellarators 不是口号竞争。

它们是对同一个 magnetic question 的两种回答。

Tokamaks 说：

> 用 plasma current 和 symmetry 产生 helical confinement。

Stellarators 说：

> 把 helical confinement 做进外部 geometry。

一个对抗 current。
另一个对抗 geometry。

两者都在试图让 magnetic field lines 表现得足够久，使 fusion 从 aspiration 变成 engineering。
