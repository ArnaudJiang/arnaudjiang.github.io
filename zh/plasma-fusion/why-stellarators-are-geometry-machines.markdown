---
layout: page
title: "为什么仿星器是几何机器"
permalink: /zh/plasma-fusion/why-stellarators-are-geometry-machines/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/why-stellarators-are-geometry-machines/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 15
description: "rotational transform、magnetic surfaces、3D coils 和 quasisymmetry。"
excerpt: "rotational transform、magnetic surfaces、3D coils 和 quasisymmetry。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/why-stellarators-are-geometry-machines/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# 为什么仿星器是几何机器

*rotational transform、magnetic surfaces、3D coils 和 quasisymmetry*

Stellarator 常被介绍成 tokamak 的扭曲亲戚。

视觉上这是真的，但概念上太小。

Stellarator 是一台 central design variable 是 geometry 的机器。

它的 coils 被塑造成特定形状，使 magnetic field lines 绕 torus 缠绕，形成有用 magnetic surfaces，降低 particle losses，并避免依赖大型 plasma current。

在 tokamak 中，许多 twist 由 plasma 承担。

在 stellarator 中，twist 被写进空间。

---

## 1. Rotational transform

为了 confinement，magnetic field line 不能只是 toroidally 绕圈。

它还必须 poloidally 移动，使它经过多圈后采样一个 surface，而不是停留在一条坏路径上。

这种每个 toroidal turn 对应的 poloidal advance 由 rotational transform 描述，常写作 $\iota$。

概念上：

> rotational transform 告诉我们 field lines 如何绕 torus 扭转。

Transform 不足时，particles 和 field lines 不能很好采样几何。Transform 选择不好时，resonances 可以创造 islands。

所以 stellarator design 从问 magnetic field 应有什么 transform profile 开始。

---

## 2. Magnetic surfaces

理想 stellarator 有 nested magnetic surfaces。

每个 surface 像一个 toroidal shell。Field lines 在它上面绕行。Pressure 可以近似在上面保持常数。跨 surface 的 transport 比沿 surface 的运动慢。

Nested surfaces 给 plasma 一个有序 geometry。

但 3D magnetic fields 很脆弱。

小的 resonant components 可以创造 magnetic islands。Overlapping islands 可以创造 stochastic regions。Coil errors 可以破坏 surfaces。

Stellarator 因此必须设计的不只是 field strength，而是 field topology。

Geometry 就是 confinement system。

---

## 3. Coils 作为数学对象

Stellarator coils 看起来奇怪，不是因为审美。

它们不只是把 magnets 放在正确位置。

它们在雕刻三维 magnetic field。

Coil shapes 必须同时满足许多要求：

* 创造 rotational transform；
* 保持 magnetic surfaces；
* 降低 neoclassical transport；
* 支持 MHD equilibrium；
* 允许足够 coil spacing；
* 可以制造；
* 为 blanket、diagnostics、heating 和 maintenance 留出空间。

这就是为什么 stellarator design 是 computational 的。

Coil 不是 physics 之后画出来的东西。

Coil 是 physics solution 的一部分。

---

## 4. Trapped particles 问题

在非均匀 magnetic field 中，一些 particles 会被困在 stronger-field regions 之间。

这些 trapped particles bounce。Bounce 的同时，它们也 drift。在没有优化好的 stellarator 中，这些 drifts 可以把 particles 径向带出去。

这是 transport disaster。

所以 stellarator geometry 必须被设计成让 trapped-particle drifts 有利地平均。

这就是为什么视觉上的平滑不够。

漂亮 coil shape 仍然可能是糟糕 confinement geometry。

Particles 在 phase space 中评判机器。

---

## 5. Quasisymmetry

Axisymmetry 帮助 tokamaks 约束 particles，因为它给出 conserved quantity。

Stellarators 没有真正 axisymmetry。但它们可以创造一种更弱的秩序：quasisymmetry。

在 quasisymmetric field 中，magnetic field strength 在特殊 magnetic coordinates 中具有 symmetry，即使物理形状完全三维。

目标是在不回到 tokamak 的情况下，恢复一部分 symmetry 带来的 good particle confinement。

这是一个漂亮想法：

> 让一个 3D object 对 particle motion 来说，像是有 hidden symmetry。

现代 stellarator optimization 经常围绕这个思想，以及 quasi-isodynamic design 等相关概念展开。

---

## 6. Geometry 也是 engineering

Geometry 不止于 magnetic field lines。

反应堆尺度 stellarator 还必须容纳：

* superconducting coils；
* structural supports；
* blanket modules；
* divertor and exhaust systems；
* heating access；
* diagnostics；
* remote maintenance；
* tolerances and assembly procedures。

优化后的 magnetic field 必须由真的能建造的 coils 产生。

这就是为什么 stellarators 不只是 physics puzzles。

它们是最深意义上的 geometry machines：plasma geometry、coil geometry、engineering geometry 和 maintenance geometry 全部碰撞在一起。

---

## 结尾

Stellarator 试图用设计好的 magnetic geometry 替代 plasma current。

这个交换很深。

它降低了一些 current-driven problems，但也让 geometry 对几乎所有其他东西负责：transform、surfaces、trapped particles、transport、stability、islands、coils 和 engineering access。

Stellarator 的复杂不是偶然。

它复杂，是因为它试图把 confinement 预先计算进形状里。
