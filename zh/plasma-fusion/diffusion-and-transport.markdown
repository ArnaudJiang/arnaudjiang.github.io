---
layout: page
title: "Diffusion and Transport：为什么约束是时间尺度问题"
permalink: /zh/plasma-fusion/diffusion-and-transport/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/diffusion-and-transport/
series: plasma-fusion
series_layer: modeling
series_order: 9
description: "classical diffusion、neoclassical diffusion 和 Bohm diffusion 的物理图像。"
excerpt: "classical diffusion、neoclassical diffusion 和 Bohm diffusion 的物理图像。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/diffusion-and-transport/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Diffusion and Transport：为什么约束是时间尺度问题

*classical diffusion、neoclassical diffusion 和 Bohm diffusion 的物理图像*

磁约束不只是“能不能把 plasma 关住”的问题。

它问的是：能关多久。

上一篇文章用 MHD 描述大尺度 equilibrium 和 stability。在那种语言里，如果压强梯度被磁力平衡，plasma 可以待在一个磁构型中：

$$
\nabla p = \mathbf{j}\times\mathbf{B}
$$

但 equilibrium 不等于 confinement。

Plasma 可以处在力平衡中，却仍然慢慢漏掉。

这种泄漏叫 **transport**。

Transport 是 fusion 安静的敌人。它不一定暴烈地摧毁 plasma。它可能只是把粒子、动量和热量缓慢地跨过磁面搬走，直到核心冷却、密度剖面变平，反应堆失去 fusion 所需条件。

所以 confinement 是时间尺度问题。

问题不是：

> 磁场能不能阻止所有损失？

而是：

> 磁场能不能把损失拖慢到 fusion 先发生？

---

## 1. Diffusion 是梯度的慢泄漏

Diffusion 是梯度试图抹平自己的过程。

如果核心密度高于边缘，粒子倾向于向外移动。
如果核心温度高于边缘，热量倾向于向外移动。
如果动量集中在某处，viscosity 会把它扩散开。

最简单的粒子扩散写成 Fick's law：

$$
\mathbf{\Gamma} = -D\nabla n
$$

$\mathbf{\Gamma}$ 是 particle flux，$n$ 是 density，$D$ 是 diffusion coefficient。

负号很重要。它表示通量沿梯度下降方向流动：从高密度走向低密度。

热输运也有类似形式：

$$
\mathbf{q} = -\chi n \nabla T
$$

这里 $\mathbf{q}$ 是 heat flux，$T$ 是 temperature，$\chi$ 是 thermal diffusivity。

这已经足够说明 fusion 为什么困难。Fusion plasma 需要强梯度。核心必须极热，壁面必须仍然是物质。但梯度正是 transport 想要松弛的东西。

Fusion 是让一种有用的 non-equilibrium state 活下来的艺术。

---

## 2. 为什么磁场会降低 diffusion

普通中性气体中，粒子碰撞后可以向任意方向游走。

磁化 plasma 中，带电粒子绕磁力线回旋。跨磁场运动受到限制。它们不能自由横穿 $B$，而是以 Larmor radius 回旋：

$$
r_L = \frac{mv_\perp}{\lvert q\rvert B}
$$

因此 cross-field diffusion 远小于 parallel diffusion。

沿磁场方向，粒子可以很容易 streaming：

$$
D_\parallel \sim v_{\mathrm{th}}^2 \tau
$$

垂直磁场方向，同样的碰撞会被 gyromotion 过滤。一个有用的 classical estimate 是：

$$
D_\perp
\sim
\frac{D_\parallel}{1+\omega_c^2\tau^2}
$$

在 strongly magnetized limit 中，

$$
\omega_c\tau \gg 1
$$

它变成：

$$
D_\perp \sim \frac{v_{\mathrm{th}}^2}{\omega_c^2 \tau}
$$

由于 $r_L \sim v_{\mathrm{th}}/\omega_c$，同一个 scaling 也可以写成：

$$
D_\perp \sim \frac{r_L^2}{\tau}
$$

最后这个形式应该被理解成 scaling argument，而不是说每一次碰撞都精确地把 guiding center 移动一个 Larmor radius。重点是 cross-field diffusion 被下面这个因子压低：

$$
\frac{D_\perp}{D_\parallel}
\sim
\frac{1}{\omega_c^2\tau^2}
$$

这里 $\omega_c$ 表示 cyclotron frequency，也就是粒子绕磁场回旋的角频率：

$$
\omega_c = \frac{\lvert q\rvert B}{m}
$$

$\tau$ 表示 collision time，也就是两次有效碰撞之间的典型时间。所以 $\omega_c\tau$ 大致表示：一个粒子在两次碰撞之间能完成多少次回旋。

磁场越强，Larmor radius 越小，碰撞就越难把粒子跨磁力线搬走。

这就是 magnetic confinement 的基本承诺。

磁场不会停止运动。
它让错误方向的运动变得昂贵。

---

## 3. Classical diffusion：乐观答案

最简单的 cross-field transport 理论是 **classical diffusion**。

它想象粒子绕磁力线回旋，偶尔碰撞。每次碰撞稍微改变 guiding center。经过许多次碰撞，guiding center 在垂直磁场方向做 random walk。

其尺度大致为：

$$
D_\perp \propto \frac{1}{B^2}
$$

这很鼓舞人。

如果 transport 像 $1/B^2$ 一样下降，那么更强的磁体应该显著改善 confinement。

但实验很快发现，真实磁约束装置中的粒子和热损失常常比 classical diffusion 预测快得多。

这并不意味着 classical diffusion 没用。

它给出基线：在简单磁化 plasma 中，由局域碰撞产生的 transport。

当实验超过这个基线，问题就变成：

> 简单图像忘记了什么？

答案是 geometry、trapped particles、electric fields、turbulence 和 collective motion。

Classical diffusion 是第一估计。
Fusion devices 活在修正项里。

---

## 4. Ambipolar diffusion：电子和离子不能各漏各的

电子比离子轻。如果它们是中性粒子，会扩散得快得多。

但 plasma 不能随便分离电荷。

如果电子比离子更快离开某区域，就会产生电场。这个电场把电子拉回去，同时推动离子跟上。Plasma 倾向于保持 quasineutrality：

$$
n_i \approx n_e
$$

这种耦合损失叫 **ambipolar diffusion**。

核心想法很简单：

> 在 plasma 中，不同 species 不能长时间独立输运，因为电荷分离会产生场，把它们重新耦合。

所以 plasma transport 不是普通气体扩散加上一些符号。

通量产生场。
场改变通量。
泄漏是自洽的。

---

## 5. Neoclassical diffusion：几何进入 transport problem

Classical diffusion 假设磁场相对简单。

Toroidal confinement 并不简单。

在 torus 中，磁场强度沿装置变化。粒子可能被困在 magnetic mirror 区域。它们的轨道不只是绕磁力线的小圆，而是会 bounce、drift，并以复杂方式采样几何。

这产生 **neoclassical transport**。

这个词听起来像小修正，但概念上是大步：

> Transport 不再只是局域碰撞加 Larmor motion，而是 collisions plus orbit geometry。

Tokamak 中，trapped particles 走 banana-shaped orbits。其径向宽度可能远大于 Larmor radius。碰撞把粒子散射进出 trapped regions，产生超过 classical estimates 的 transport。

Stellarator 中，neoclassical transport 对几何更加敏感。因为磁场完全三维，trapped-particle drifts 可能造成显著径向损失，除非几何经过仔细优化。

这就是为什么 stellarators 是 geometry machines。

它们不只是要制造好的 magnetic surfaces。
它们还要让粒子轨道缓慢损失能量。

---

## 6. Bohm diffusion：经验警告

Classical diffusion 暗示：

$$
D_\perp \propto \frac{1}{B^2}
$$

但许多早期实验发现 transport 更接近：

$$
D_B \sim \frac{k_B T}{16 e B}
$$

这叫 **Bohm diffusion**。

它的尺度是：

$$
D_B \propto \frac{T}{B}
$$

这对 confinement 糟糕得多。

Bohm diffusion 的意义不是说每个 plasma 都严格遵守这个公式。它的意义是：实验揭示的 cross-field transport 远大于最简单碰撞理论预期。

Bohm diffusion 是警铃。

它说：

> 有某种 collective process 正在把 plasma 跨磁场搬走。

今天，我们常常用 turbulence、fluctuations、instabilities 和相关的 $E\times B$ motion 来理解这些过程。Plasma 不是只靠碰撞一点点横穿磁力线。它在振动、旋涡化、重新排列自身。

Transport 常常不是逐个粒子的泄漏。
它是集体泄漏。

---

## 7. Transport 不只是粒子损失

说到 confinement，人们容易只想到粒子逃逸。

但 fusion 尤其关心 **energy confinement**。

Plasma 可以保留大部分粒子，却损失太多热量。

Transport 有许多通道：

* particle transport：密度剖面变化；
* heat transport：温度剖面变化；
* momentum transport：流动和旋转变化；
* current transport：电流剖面演化；
* impurity transport：重离子进入或离开核心。

这些通道互相耦合。

Heat transport 改变 pressure。
Pressure 改变 equilibrium 和 stability。
Impurity transport 改变 radiation losses。
Current transport 改变 magnetic shear。
Momentum transport 改变 flows，而 flows 可能抑制或增强 turbulence。

所以 fusion modeling 必然是分层的。

MHD 问大尺度构型能不能活下来。
Transport 问剖面能不能活得足够久。

---

## 8. Confinement time

表达 transport 痛苦最紧凑的量是 energy confinement time：

$$
\tau_E = \frac{W}{P_{\mathrm{loss}}}
$$

其中 $W$ 是 stored plasma energy，$P_{\mathrm{loss}}$ 是 plasma 损失功率。

如果 $\tau_E$ 太小，plasma 冷却速度就会超过 heating 和 fusion power 的维持能力。

Lawson criterion 通常用 density、temperature 和 confinement time 表示。一个常见概念形式是，fusion 需要足够大的 triple product：

$$
nT\tau_E
$$

所以 confinement 不只是空间问题。

它是时间问题。

Plasma 不需要被永远关住。它需要在足够高的 density 和 temperature 下，被关得足够久，让 fusion power 变得有意义。

这才是 magnetic-confinement dream 更精确的版本：

> keep the plasma hot enough, dense enough, and long enough.

---

## 9. 为什么梯度既必要又危险

Transport 存在，因为 gradients 存在。

Fusion 需要 gradients。

核心必须热。边缘必须较冷。Density 和 pressure 必须横跨 plasma 变化。Heating 非均匀沉积。粒子和 impurities 通过边界进出。

但 gradients 含有 free energy。

Pressure gradient 可以驱动 drift waves。
Temperature gradient 可以驱动 ion-temperature-gradient turbulence。
Density gradient 可以驱动 trapped-electron modes。
Current gradients 可以驱动 tearing modes。

所以 gradients 是双刃剑。

没有 gradients，就没有有用的 confined plasma。
有了 gradients，就有 free energy 可以驱动 transport。

任务不是消灭 gradients。

任务是塑造它们，使 plasma 仍然有用。

---

## 10. 为什么 stellarators 如此关心 transport

Stellarator 试图主要用外部线圈创造 confinement，而不是依赖大型 plasma current。

这有利于 steady-state operation，也能降低某些 current-driven instabilities。

但这让 geometry 变成一切。

磁场是三维的。Trapped particles 可以径向漂移。几何上的小变化可能强烈影响 neoclassical transport。Ripple、islands 和 broken flux surfaces 都可能变成 transport paths。

因此现代 stellarator optimization 不只问：

> 有没有 nested magnetic surfaces？

还会问：

> Trapped particle orbits 是否仍被约束？Neoclassical transport 是否足够小？Turbulent drives 是否降低？好的 confinement 能不能与 MHD stability 和工程约束共存？

这就是为什么 stellarator design 像 computational geometry、plasma physics 和 optimization theory 的融合。

装置不只是在设计磁场。

它在设计 transport landscape。

---

## 结尾

MHD 告诉我们，被约束的 plasma 必须满足力平衡，并在扰动下存活。

Transport 告诉我们，即使稳定的 plasma 也可能输掉时间竞赛。

粒子扩散。
热量泄漏。
动量铺开。
杂质移动。
电流演化。
Turbulence 找到 gradients，并把它们变成 flux。

所以 confinement 不是 yes-or-no property。

它是 time scale。

Fusion 问的是，plasma 能否保持足够热、足够密、足够久，让反应回报 confinement 的成本。

这就是为什么 transport 是从漂亮磁几何走向反应堆现实的桥。
