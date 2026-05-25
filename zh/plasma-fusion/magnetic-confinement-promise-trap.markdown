---
layout: page
title: "Magnetic Confinement：希望与陷阱"
permalink: /zh/plasma-fusion/magnetic-confinement-promise-trap/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/magnetic-confinement-promise-trap/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 13
description: "为什么磁场有用，以及为什么环形几何会产生漂移损失。"
excerpt: "为什么磁场有用，以及为什么环形几何会产生漂移损失。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/magnetic-confinement-promise-trap/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Magnetic Confinement：希望与陷阱

*为什么磁场有用，以及为什么环形几何会产生漂移损失*

Magnetic confinement 从一个漂亮事实开始：

带电粒子不能自由横跨磁场。

它们 gyrate。Guiding centers 沿 field lines 运动。Cross-field motion 缓慢、有结构，并常常以 drift 形式出现。这提示一个简单梦想：

> 让 magnetic field lines 避开 wall，plasma 就会避开 wall。

这个梦想正确到足以建造装置。

也不完整到足以支撑整个领域。

---

## 1. 磁场给了我们什么

对带电粒子：

$$
m\frac{d\mathbf{v}}{dt}
=
q(\mathbf{E}+\mathbf{v}\times\mathbf{B})
$$

Lorentz force 的 magnetic part 垂直于 velocity。它弯曲轨道，而不直接做功。

在均匀磁场中，带电粒子以 Larmor radius 回旋：

$$
r_L = \frac{mv_\perp}{\lvert q\rvert B}
$$

更强的 $B$ 意味着更小 gyro-orbits。Cross-field wandering 更难。

这就是 promise：

> magnetic fields 把自由逃逸变成受约束运动。

---

## 2. 直磁场会从端部漏掉

Straight magnetic field 约束垂直运动，但不约束平行运动。

粒子容易沿 field lines streaming。如果 field line 碰到 wall，粒子就会到达 wall。

所以简单 solenoid 不够。除非处理端部，否则 plasma 会沿 field 逃走。

一种答案是 mirror machine：让端部磁场更强，使一部分粒子反射。

但 mirror confinement 有 loss cones。Parallel velocity 足够大的粒子会逃逸。

另一种答案是闭合 field lines。

这就导向 torus。

---

## 3. Torus 解决一个问题，又创造另一个

Torus 移除了端部。

Field lines 可以绕装置转圈，不撞 end plates。乍看这是显然答案。

但 torus 是弯曲的。

内侧 magnetic field 更强，外侧更弱。Field lines 有 curvature。Grad-$B$ drift 和 curvature drift 出现。Ions 和 electrons 以相反 vertical directions 漂移，造成 charge separation 和 electric fields。这些 electric fields 驱动 $E\times B$ motion。

移除 end loss 的装置，引入 drift loss。

这就是 trap。

Toroidal confinement 不是把 solenoid 弯成圆那么简单。

它是带有新 plasma motion 的新 geometry。

---

## 4. 为什么 twist 重要

为了避免粒子系统性向外 drift，magnetic field lines 必须采样 torus 的不同区域。

它们需要 twist。

Tokamak 中，twist 主要来自 plasma current 产生的 poloidal magnetic field，并与外部 toroidal field 结合。

Stellarator 中，twist 主要由外部三维 coils 产生。

无论哪种方式，目标类似：

> 让 field lines 螺旋绕 torus，使 radial drifts 被平均，而不是积累。

这就是为什么 magnetic confinement 变成 field-line geometry 问题。

问题不只是 $B$ 有多强。

而是 $B$ 的 geometry 是否能让 particle motion 在许多轨道后仍然表现良好。

---

## 5. Magnetic surfaces

理想 confinement geometry 有 nested magnetic surfaces。

Particles 和 field lines 在 surfaces 上绕行，而不是径向乱走撞 wall。Pressure 可以按 surface label 组织。跨 surfaces 的 transport 相比沿 surfaces 的快速运动更慢。

这是 magnetic confinement 的几何核心：

> fast motion along surfaces, slow leakage across surfaces.

但 magnetic surfaces 可以被破坏。

Resonances 可以创造 islands。Perturbations 可以让 field lines stochastic。Instabilities 可以毁掉有序几何。

所以 confinement 不只是创造 magnetic surfaces。

它还要在 plasma pressure、current、turbulence 和 engineering imperfections 下保住它们。

---

## 6. Edge 是 trap 的一部分

即使 core 被很好约束，heat 和 particles 最终也必须离开。

反应堆必须排出 helium ash，控制 impurities，并处理 heat loads。Plasma edge 必须以受控方式连接到 material components。

这创造了张力：

core 想要 isolation，
edge 需要 exhaust。

Magnetic confinement 因此必须同时做两件相反的事：

* 让 hot core 远离 walls；
* 把不可避免的 losses 引导到能承受的位置。

这就是 divertors、scrape-off layers、islands 和 edge control 如此重要的原因。

Boundary 不是事后问题。

它是 confinement 变成 engineering 的地方。

---

## 7. 希望与陷阱

希望是真的。

Magnetic fields 可以让 cross-field transport 降低许多数量级。它们可以在没有 material contact 的情况下创造长 confinement time。它们让 controlled fusion 变得可想象。

陷阱也是真的。

约束粒子的几何也会创造 drifts。创造 twist 的 currents 也会驱动 instabilities。Fusion 所需 gradients 会驱动 turbulence。组织 plasma 的 magnetic surfaces 也可能被破坏。

Magnetic confinement 强大，因为 plasma 带电。

它困难，也是同一个原因。

Plasma 在 field 中不是被动的。

它运动、漂移、导电、回应，并且反推。

---

## 结尾

Magnetic fields 有用，因为它们约束 charged-particle motion。

Toroidal geometry 有用，因为它移除 end losses。

Twist 有用，因为它平均 drifts。

但每一层帮助都会创造下一层 physics。

这就是 trap：magnetic confinement 不是一个解决方案，而是一串解决方案，每一个都暴露下一个问题。

Tokamaks 和 stellarators 是沿着这条链走的两种方式。
