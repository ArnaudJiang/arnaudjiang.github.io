---
layout: page
title: "绝热不变量：粒子轨道中的隐藏约束"
permalink: /zh/plasma-fusion/adiabatic-invariants/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/adiabatic-invariants/
series: plasma-fusion
series_layer: conceptual
series_order: 5
description: "magnetic moment、bounce invariant、flux invariant，以及它们为什么支撑 mirror、trapped particles 和磁约束直觉。"
excerpt: "magnetic moment、bounce invariant、flux invariant，以及它们为什么支撑 mirror、trapped particles 和磁约束直觉。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/adiabatic-invariants/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# 绝热不变量：粒子轨道中的隐藏约束

*magnetic moment、bounce invariant、flux invariant，以及它们为什么支撑 mirror、trapped particles 和磁约束直觉*

前几篇文章建立了一个图像：

磁场不会像墙一样困住粒子。
它让带电粒子回旋。
回旋轨道的中心会漂移。

但这还不是单粒子运动故事的全部。

在缓慢变化的磁场中，粒子运动并不是任意混乱的。即使轨道看起来很复杂，某些组合量也会近似保持不变。这些量叫 **adiabatic invariants**，也就是绝热不变量。

这里的“绝热”不是热力学里“没有热交换”的意思。

在单粒子运动中，它的意思更接近：

> 外部条件变化得足够慢，粒子来得及完成许多次快速周期运动，于是某个周期平均量近似守恒。

这个思想非常强。

它告诉我们，粒子不是只被瞬时力决定。它还被自己的快运动周期约束。

---

## 1. 为什么会有绝热不变量

想象一个带电粒子在磁场中快速回旋。

回旋频率是 cyclotron frequency：

$$
\Omega_c = \frac{|q|B}{m}.
$$

如果磁场在一次回旋期间几乎不变，粒子看到的环境就是近似静态的。它完成很多圈之后，磁场才有显著变化。

这种尺度分离是关键：

$$
\frac{1}{\Omega_c} \ll \tau_B,
$$

其中 $\tau_B$ 是磁场变化的时间尺度，或者粒子沿轨道看到磁场显著变化的有效时间尺度。

当快运动和慢变化分离时，快运动的相位细节可以被平均掉。平均之后，系统会保留一些近似守恒的 action-like quantities。

对磁化粒子来说，最重要的三个绝热不变量对应三个逐渐更慢、更大的周期：

1. 回旋运动；
2. bounce motion；
3. drift motion。

它们分别给出第一、第二、第三绝热不变量。

---

## 2. 第一绝热不变量：磁矩

第一绝热不变量是 **magnetic moment**：

$$
\mu = \frac{mv_\perp^2}{2B}.
$$

这里 $v_\perp$ 是粒子相对于磁场的垂直速度。

这个量的直觉很简单：回旋粒子像一个小电流环。电流环有磁矩。只要磁场变化足够慢、足够平滑，这个磁矩近似守恒。

所以如果粒子进入更强的磁场区域，$B$ 增大。为了让 $\mu$ 保持不变，$v_\perp^2$ 也必须增大。

粒子的垂直能量增加。

总能量如果没有外部电场做功，就近似守恒。于是平行能量必须减少：

$$
\frac{1}{2}mv^2
=
\frac{1}{2}mv_\perp^2
+
\frac{1}{2}mv_\parallel^2.
$$

这就是 magnetic mirror 的核心。

强磁场不是像墙一样把粒子反弹回去。它通过磁矩守恒把平行动能转成垂直动能。当 $v_\parallel$ 降到零，粒子不能继续进入更强场区，就会反向运动。

---

## 3. Mirror motion：反射来自守恒量

设粒子从弱场区进入强场区。

如果 $\mu$ 守恒，那么

$$
\frac{mv_\perp^2}{2B}
=
\text{constant}.
$$

当 $B$ 增大，$v_\perp^2$ 增大。

如果总能量不变，$v_\parallel^2$ 下降。

在某一点，可能出现

$$
v_\parallel = 0.
$$

这就是 mirror point。

从概念上说，mirror force 沿磁场方向把粒子从强场区推回弱场区。它可以写成近似形式：

$$
F_\parallel = -\mu \nabla_\parallel B.
$$

这条公式值得慢慢看。

粒子并没有直接感受到一个普通机械镜面。
它感受到的是磁场强度沿磁力线变化带来的有效力。

更强的磁场区域会排斥具有足够大垂直能量的粒子。

这解释了为什么 magnetic mirror 可以约束一部分粒子，也解释了为什么它不能约束所有粒子。

如果一个粒子的 $v_\parallel$ 太大、$v_\perp$ 太小，它就不容易被反射。它会穿过 mirror region，从端部逃逸。

这就是 loss cone。

---

## 4. Loss cone：不是所有粒子都会被镜像

用 pitch angle 描述粒子速度方向：

$$
\sin^2\alpha = \frac{v_\perp^2}{v^2}.
$$

如果粒子起始处磁场为 $B_0$，mirror point 处磁场为 $B_m$，则能被反射的条件大致是：

$$
\sin^2\alpha_0 \ge \frac{B_0}{B_m}.
$$

垂直速度成分足够大的粒子会被反射。

平行速度成分太大的粒子会落入 loss cone。

这给 magnetic confinement 一个非常重要的教训：

> 磁场几何不只约束空间位置，也筛选速度空间。

两个粒子从同一个位置出发，如果 pitch angle 不同，命运可能完全不同。

这也是为什么 kinetic theory 后面会变得不可避免。流体变量可能只告诉我们密度和温度，但 loss cone 是速度空间里的结构。它不能只靠一个标量压力完整描述。

---

## 5. 第二绝热不变量：bounce invariant

如果一个粒子被两个 mirror point 困住，它会沿磁力线来回 bounce。

这个 bounce motion 比 Larmor gyration 慢，但仍然可以是周期性的。

当磁场结构沿粒子 bounce 轨道变化得足够慢时，会出现第二绝热不变量：

$$
J = \oint mv_\parallel\, ds.
$$

积分沿粒子在两个 mirror point 之间的一次往返路径进行。

直觉上，$J$ 衡量的是平行运动在一个 bounce 周期中的 action。

第一绝热不变量约束回旋运动。
第二绝热不变量约束 bounce motion。

这对 trapped particles 很重要。

在 tokamak 或 stellarator 中，磁场强度沿磁力线变化。一些粒子会因为磁镜效应被困在低场区域附近，沿磁力线来回反弹，而不是绕整个 torus 自由 passing。

这些 trapped particles 的漂移、碰撞和输运行为与 passing particles 不同。

所以绝热不变量不是数学装饰。它们直接决定粒子种群。

---

## 6. 第三绝热不变量：flux invariant

第三绝热不变量对应更慢的 drift motion。

如果粒子的 guiding center 围绕一个封闭区域缓慢漂移，并且磁场变化仍然比这个 drift 周期慢，那么粒子 drift orbit 包围的 magnetic flux 可以近似守恒。

常见的直觉写法是：

$$
\Phi = \oint \mathbf{A}\cdot d\mathbf{l}
$$

或者说，粒子漂移轨道所围住的磁通近似不变。

这个不变量通常比前两个更脆弱。

原因很直接：它依赖最大的空间尺度和最慢的周期。真实磁约束装置中，碰撞、湍流、三维 ripple、岛、随机场线和时间变化扰动都可能破坏它。

但它仍然是一个有用的概念。

它把单粒子运动和磁通面联系起来：如果 drift orbit 围住的磁通能保持不变，粒子就更容易长期留在同一类磁面附近。如果这个约束被破坏，径向输运就会增强。

---

## 7. 绝热不变量什么时候失效

绝热不变量是近似，不是契约。

它们要求几个条件：

1. 场在一个周期内变化很小；
2. 空间尺度远大于相关轨道尺度；
3. 碰撞和强扰动足够弱；
4. 粒子没有穿过破坏周期运动的 separatrix 或强 resonance。

第一绝热不变量要求磁场在 Larmor 半径上平滑。
第二绝热不变量要求 bounce motion 保持清晰。
第三绝热不变量要求 drift orbit 有足够好的封闭结构。

当这些条件失败时，不变量会被破坏。

这就是为什么边缘、强湍流、磁岛、stochastic field lines、强波粒共振和碰撞都很危险。它们不是简单地“扰动粒子”。它们会破坏粒子轨道中的慢守恒结构。

一旦守恒结构被破坏，粒子就更容易在相空间中扩散。

约束也就变差。

---

## 8. 为什么这对 stellarator 特别重要

Stellarator 是三维磁几何机器。

它的目标不是制造一个简单漂亮的磁场，而是制造一个在相空间中足够好的磁场。

这句话的意思是：我们不只关心磁力线看起来是否闭合，也不只关心磁场强度是否大。我们关心 trapped particles、drift orbits、bounce motion 和 neoclassical transport 是否会产生不可接受的径向损失。

绝热不变量正是连接这些问题的语言。

第一不变量告诉我们粒子如何在强弱磁场之间交换平行和垂直能量。
第二不变量告诉我们 trapped particles 的 bounce motion 如何保持结构。
第三不变量告诉我们 drift orbit 是否仍然与磁通面保持联系。

如果几何不好，trapped particles 的 drift 可以系统性地向外偏移。
如果几何足够优化，这些偏移可以在一个 bounce 或 drift 周期中平均掉。

这就是 quasisymmetry、omnigeneity 和 stellarator optimization 背后的核心动机之一：

> 设计磁场，使粒子的绝热轨道结构尽可能不把它们送向壁面。

---

## 9. 概念上的结论

Drifts 告诉我们，导引中心会移动。

绝热不变量告诉我们，这种移动并不是完全任意的。

粒子有快速回旋、较慢 bounce 和更慢 drift。每一层周期运动，在足够缓慢、足够平滑的背景中，都可能留下一个近似守恒量。

这些守恒量让磁约束有希望。

它们也暴露磁约束的脆弱。

如果 $\mu$ 守恒，magnetic mirror 可以反射粒子。
如果 $J$ 守恒，trapped-particle motion 有可预测结构。
如果 drift flux 近似守恒，粒子更可能停留在好的磁面附近。

但如果碰撞、湍流、共振或三维不完美破坏这些不变量，粒子会在相空间中扩散，输运会增加，约束会恶化。

所以绝热不变量不是一段附录。

它们是从单粒子轨道走向 magnetic confinement 的关键桥梁：

磁场不只是弯曲粒子。
它也在粒子运动中创造近似守恒结构。

聚变装置的难处在于，让这些结构在真实、热、弱碰撞、三维、自洽的等离子体中仍然足够可靠。
