---
layout: page
title: "The Stellarator Transport Problem"
permalink: /zh/plasma-fusion/stellarator-transport-problem/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/stellarator-transport-problem/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 16
description: "drift、magnetic mirror、adiabatic invariant 和 neoclassical transport。"
excerpt: "drift、magnetic mirror、adiabatic invariant 和 neoclassical transport。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/stellarator-transport-problem/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# The Stellarator Transport Problem

*drift、magnetic mirror、adiabatic invariant 和 neoclassical transport*

Stellarator 的 promise 是：不依赖大型 plasma current，也能实现 steady magnetic confinement。

Stellarator 的 price 是：transport。

因为 magnetic field 完全三维，particle orbits 会变得复杂。Particles 可能被困在 magnetic wells 中，径向 drift，并以造成损失的方式采样 field，即使 magnetic surfaces 存在。

这就是为什么 stellarator design 如此执着于 orbit quality。

Field lines 看起来被约束还不够。

Particles 也必须同意。

---

## 1. Field lines 不是 particle orbits

Magnetic field line 是几何曲线。

Charged particle 会绕 field line gyrate，沿着它 streaming，跨过它 drift，并响应 electric fields、pressure gradients 和 collisions。

所以好的 field-line geometry 不自动意味着好的 particle confinement。

Guiding center 有自己的 dynamics。

这个区别在 stellarators 中很核心，因为 3D magnetic fields 会创造 trapped-particle behavior，而如果只看 field lines，这些行为可能不可见。

Field line 也许留在 surface 上。

Particle 的 guiding center 未必。

---

## 2. Magnetic mirrors 和 trapped particles

如果粒子进入更强 magnetic field，它的 perpendicular energy 增加，parallel motion 可能变慢。

Magnetic moment：

$$
\mu = \frac{mv_\perp^2}{2B}
$$

在 field 相对 gyromotion 缓慢变化时近似守恒。

这个 adiabatic invariant 解释 magnetic mirroring。

有足够 perpendicular energy 的 particles 可以在 high-field regions 之间 bounce。这些就是 trapped particles。

在 stellarator 中，$B$ 的三维变化创造许多可能 trapping structures。Trapped particles bounce、drift、collide。它们的 averaged radial motion 是 neoclassical transport 的主要来源。

---

## 3. 为什么 trapped-particle drifts 重要

Curvature 和 grad-$B$ drifts 依赖 charge、energy、magnetic field strength 和 geometry。

在 axisymmetric tokamak 中，symmetry 给出 conserved quantity，有助于让 guiding-center orbits 保持 bounded。

在一般 stellarator 中，这种保护更弱。

Trapped particle 可以在 magnetic well 中 bounce，同时 drift 有 radial component。经过许多 bounce，这个 radial drift 可以把它带过 flux surfaces。

这就是基本 stellarator transport problem：

> confinement 所需的 3D geometry，也可能创造 orbit losses。

现代 stellarators 被设计来降低这些不良 averaged drifts。

---

## 4. Stellarator 中的 neoclassical transport

Neoclassical transport 是 collisions 作用在 toroidal geometry 中 particle orbits 上产生的 transport。

在 stellarators 中，neoclassical transport 可能很大，因为 trapped-particle orbits 对 3D magnetic field 很敏感。

Collisions 把 particles 在 trapped 和 passing classes 之间散射。Electric fields 改变 radial motion。不同 collisionality regimes 产生不同 scaling laws。

这就是为什么 stellarator 不能只用 MHD equilibrium 判断。

它必须用 neoclassical confinement 判断。

问题变成：

> 加入真实 guiding-center orbits 和 collisions 后，particles 还能不能被约束？

---

## 5. Optimization targets

Stellarator optimization 试图塑造 magnetic field，使 particle losses 小。

重要思想包括：

* 降低 trapped particles 的 radial drift；
* 创造 quasisymmetry 或 quasi-isodynamic behavior；
* 保持 nested flux surfaces；
* 控制 magnetic islands；
* 管理 bootstrap current；
* 让 turbulent transport 可接受；
* 满足 coil 和 engineering constraints。

这不是一个目标。

这是许多目标之间的 negotiated settlement。

所以 stellarator design 是 optimization problem，不是 drawing problem。

---

## 6. Ambipolar electric field

Ions 和 electrons 通常不会有完全相同 radial transport。

如果某个 species 径向移动更快，就会积累 charge separation。Plasma 会通过建立 radial electric field 来调整 fluxes，使其接近 ambipolarity。

这个 radial electric field 会影响 particle orbits 和 transport。

所以 stellarator transport 不只是 magnetic geometry。

它也是 electrostatic self-consistency。

Plasma 再一次拒绝被动。

它会回应自己的损失。

---

## 7. Turbulence 仍然重要

优化 neoclassical transport 不会消除 turbulent transport。

Temperature 和 density gradients 可以驱动 microinstabilities。Turbulent $E\times B$ flows 可以把 heat 跨 flux surfaces 搬走。一个 neoclassical confinement 很好的 configuration，仍然可能受 turbulence 限制。

这是现代前沿之一：

> stellarator geometry 能否同时为 neoclassical 和 turbulent transport 优化？

答案不是自动的。

不同 loss channels 对不同 geometric features 响应。

---

## 结尾

Stellarator transport problem 是 geometry problem 的 particle-orbit 版本。

Stellarator 必须让 field lines 表现良好。

然后必须让 guiding centers 表现良好。

然后必须让 collisional transport 表现良好。

然后必须让 turbulent transport 表现良好。

这串要求就是 stellarators 困难的原因。

也是它们迷人的原因：装置试图把 geometry 变成 confinement time。
