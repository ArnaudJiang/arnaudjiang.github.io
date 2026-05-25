---
layout: page
title: "为什么聚变是约束问题"
permalink: /zh/plasma-fusion/why-fusion-is-a-confinement-problem/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/why-fusion-is-a-confinement-problem/
series: plasma-fusion
series_layer: fusion-stellarator
series_order: 12
description: "先讲温度、密度和能量约束时间，再进入装置细节。"
excerpt: "先讲温度、密度和能量约束时间，再进入装置细节。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/why-fusion-is-a-confinement-problem/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# 为什么聚变是约束问题

*先讲温度、密度和能量约束时间，再进入装置细节*

Fusion 很容易描述，却很难变得有用。

轻核靠得足够近时，强相互作用可以压过静电排斥，于是发生聚变。在恒星里，gravity 提供约束。在地球上，gravity 对反应堆尺度几乎没用。我们必须创造一个高温、高密度 plasma，并把它保持足够久，让 fusion reactions 回报输入的能量成本。

所以 fusion 首先不是 machine problem。

它是 confinement problem。

在 tokamak、stellarator、laser、blanket、turbine 或 power plant 之前，有一个更紧凑的问题：

> Plasma 能不能足够热、足够密、并且维持足够久？

---

## 1. 首先重要的三个量

最先出现的 fusion variables 不是装置名字或几何类型。

它们是：

* temperature；
* density；
* energy confinement time。

Temperature 衡量 ions 是否有足够 kinetic energy，以足够概率越过 Coulomb barrier。Density 衡量有多少可能反应的离子对。Energy confinement time 衡量 plasma 失去 stored thermal energy 的速度有多慢。

常见的概念形式是 triple product：

$$
nT\tau_E
$$

其中 $n$ 是 density，$T$ 是 temperature，$\tau_E$ 是 energy confinement time。

它不是完整反应堆故事，但表达了中心压力：

> fusion 需要足够多的粒子、每个粒子足够高的能量、以及足够长的时间。

---

## 2. Temperature 不是普通热

Fusion temperature 对日常尺度来说极其巨大。

对 deuterium-tritium fusion，有用的温度尺度在 tens of keV，约等于数亿 K。此时物质不是中性气体，而是 plasma：ions 和 electrons 集体运动，产生 fields，支持 waves，并携带 currents。

所以“加热燃料”不是加热空气。

Ions 必须足够热才能 fusion。
Electrons 可能通过 radiation 和 transport 带走能量。
Plasma 必须保持 quasineutral。
Magnetic field 必须把 charged particles 从 material walls 旁边移开。

Temperature 因此不只是 thermodynamics。

它是 plasma dynamics。

---

## 3. Density 有帮助，但不是免费的

Fusion reaction rate 随 density 增加，因为更多 ions 意味着更多可能反应对。

非常粗略地，fusion power density 满足：

$$
P_f \propto n^2 \langle\sigma v\rangle
$$

其中 $\langle\sigma v\rangle$ 是 reactivity。

这个 $n^2$ 很诱人。增加 density，fusion 增长更快。

但 density 不是免费的。

更高 density 会改变 pressure：

$$
p \sim nT
$$

更高 pressure 会更强地推磁场，改变 MHD equilibrium，可能驱动 instabilities，也可能在有 impurities 时增加 radiation losses。

所以 density 只有在 confinement 和 stability 能承受时才有用。

Fusion 充满带账单的礼物。

---

## 4. Energy confinement time 是时钟

在简单 fully ionized plasma 中，stored plasma energy 可以概念性写成：

$$
W \sim 3nTV
$$

具体因子取决于约定和 profiles。

Energy confinement time 是：

$$
\tau_E = \frac{W}{P_{\mathrm{loss}}}
$$

它回答的是：

> 如果 heating 停止，在当前 loss rate 下 plasma 需要多久失去 stored energy？

这就是 transport 为什么重要。

即使 plasma 达到 fusion temperature，如果热量太快漏掉，也没有用。Energy confinement 是判断反应堆是在赢，还是只是在昂贵地发光的时钟。

---

## 5. Lawson idea

Lawson criterion 用 density 和 confinement time 捕捉 net energy gain 的条件，temperature 通过 reactivity 和 energy balance 进入。

精确形式取决于 fuel、假设、radiation、heating efficiency，以及“gain”的定义。但直觉很稳定：

> plasma 必须在失去能量前产生足够 fusion power。

这就是为什么 magnetic confinement 和 inertial confinement 看起来完全不同，却共享同一底层逻辑。

Magnetic confinement 用较低 density 和较长 time。
Inertial confinement 用极高 density 和极短 time。

路径不同。
比赛相同。

---

## 6. 为什么 wall 不能直接关住 plasma

Fusion plasma 太热，不能接触材料。

如果 hot core 接触 wall，wall 会冷却 plasma，plasma 也会破坏 wall。所以 confinement 必须是间接的。

Magnetic confinement 使用 Lorentz force。带电粒子容易沿磁力线运动，却很难横跨磁力线。希望是设计 magnetic geometry，让 particles 和 heat 远离 wall 足够久。

但 wall 从来不是无关的。

Edge、exhaust、impurities、plasma-facing components 和 heat loads 都重要。Magnetic confinement 没有消灭 wall problem；它只是把最热的问题从 wall 移开。

这个区别很关键。

---

## 7. 为什么 magnetic confinement 变成 geometry

如果磁力线是直的，粒子会沿着端部 streaming 出去。

所以 confinement devices 会把 field 弯成闭合或近似闭合路径。这把我们推向 toroidal geometry。

但 toroidal geometry 又创造新问题：curvature、grad-$B$ drift、trapped particles、current profiles、magnetic shear、islands 和 instabilities。

防止端部损失的几何，会创造 drift 和 stability 问题。

Fusion 的反复模式是：

> 每个解决方案都会变成新的 plasma physics problem。

Tokamaks 和 stellarators 是这个 geometry problem 的两种主要答案。

---

## 8. Fusion 是 profile problem

反应堆约束的不是一个叫 “the plasma” 的数字。

它约束的是 profiles：

* density profile；
* temperature profile；
* pressure profile；
* current profile；
* impurity profile；
* rotation profile。

这些 profiles 决定 fusion power、transport、stability、radiation 和 control。

所以 equilibrium 本身不够。一个 magnetic configuration 也许存在，但 profiles 可能不稳定、损失太大，或与 exhaust 不兼容。

Fusion 要的是 living state，不是 static shape。

---

## 结尾

Fusion 难，不是因为反应本身神秘。

它难，因为 plasma 必须待在一个狭窄状态中：

足够热，才能 fuse；
足够密，才有意义；
足够安静，避免 disruption；
足够干净，避免 radiation collapse；
并且被约束足够久，赢下能量比赛。

这就是为什么每个严肃 fusion concept 最后都会回到 confinement。

Machine 是答案。
问题是 time。
