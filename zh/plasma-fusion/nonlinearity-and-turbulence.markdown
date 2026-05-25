---
layout: page
title: "Nonlinearity and Turbulence：简单模型失效处"
permalink: /zh/plasma-fusion/nonlinearity-and-turbulence/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/nonlinearity-and-turbulence/
series: plasma-fusion
series_layer: modeling
series_order: 11
description: "不稳定性增长、输运，以及为什么约束常常由湍流控制。"
excerpt: "不稳定性增长、输运，以及为什么约束常常由湍流控制。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/nonlinearity-and-turbulence/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Nonlinearity and Turbulence：简单模型失效处

*不稳定性增长、输运，以及为什么约束常常由湍流控制*

到目前为止，modeling stack 已经穿过几层。

Single-particle theory 教我们带电粒子如何在给定场中运动。
Fluid theory 教我们平均 plasma quantities 如何演化。
MHD 教我们 conducting fluid 如何平衡 pressure 和 magnetic force。
Transport theory 告诉我们 confinement 是 time-scale problem。
Kinetic theory 重新打开 velocity space，说明 resonant particles 为什么重要。

但还有一个问题。

这些模型在 disturbances 很小时最舒服。

小扰动可以 linearize。Modes 可以分离。Growth rates 可以计算。Stability boundaries 可以画出来。

然后 plasma 开始做 plasma 会做的事。

扰动增长。
Modes 耦合。
Gradients 变陡。
Eddies 形成。
Fields 重排。
Transport 改变最初驱动 instability 的 profiles。

系统开始回应自己。

这就是 nonlinearity。

当 nonlinear interactions 把能量扩散到多个尺度，并产生不规则集体运动时，我们称之为 turbulence。

对 fusion 来说，turbulence 不是背景噪声。

它常常就是决定 confinement 的东西。

---

## 1. Linear theory 是第一声警告，不是最终故事

Linear stability theory 从一个 equilibrium 出发，加上小扰动：

$$
\delta f,\quad \delta n,\quad \delta \phi,\quad \delta \mathbf{B}
$$

如果扰动满足：

$$
\delta(t) \sim e^{\gamma t}
$$

那么 $\gamma$ 是 growth rate。

如果 $\gamma < 0$，扰动被阻尼。
如果 $\gamma > 0$，扰动增长。

这极其有用。

它告诉我们哪些 gradients、currents 或 distribution functions 含有 free energy。它告诉我们哪些 modes 危险。它告诉我们扰动变大前的早期行为。

但 linear theory 不能回答最重要的下一个问题：

> Mode 增长之后会发生什么？

答案可能是 saturation、collapse、profile relaxation、magnetic reconnection、turbulence，或者一个新的 equilibrium。

Linear theory 看见门打开。
Nonlinear theory 问走进来的是什么。

---

## 2. Plasma 为什么 nonlinear

Plasma nonlinear，是因为运动的介质创造推动它的场。

在 fluid language 中，convective derivative 本身就是 nonlinear：

$$
\mathbf{v}\cdot\nabla\mathbf{v}
$$

在 MHD 中，magnetic force 是 nonlinear，因为 current 依赖 magnetic field：

$$
\mathbf{j}\times\mathbf{B}
=
\frac{1}{\mu_0}
(\nabla\times\mathbf{B})\times\mathbf{B}
$$

在 kinetic theory 中，particles 重塑 fields，fields 又重塑 distribution function：

$$
f \rightarrow \rho,\mathbf{j}
\rightarrow \mathbf{E},\mathbf{B}
\rightarrow f
$$

这种 feedback 是 plasma complexity 的核心。

Plasma 不是在响应外部剧本。

它一边表演，一边写剧本的一部分。

---

## 3. Saturation：instability 不会永远增长

Unstable mode 不可能永远指数增长。

某个时刻，nonlinear effects 会变得重要。

可能发生许多事：

* mode 抹平驱动它的 gradient；
* particles 被 wave potential 捕获；
* energy 转移到其他 modes；
* 产生 flows，并 shear turbulence；
* magnetic topology 改变；
* plasma relax 到新的 profile。

这叫 saturation。

Saturation 让 plasma physics 不再像求 eigenvalue，而更像理解一个生态系统。

Growth rate 告诉你 instability 开始得多快。

Saturation level 告诉你它造成多少 transport。

对 fusion 来说，第二个问题常常更重要。

一个快速增长但饱和振幅很小的 mode 也许可以忍受。一个增长较慢却饱和成强 transport 的 instability 可能毁掉 confinement。

---

## 4. Drift-wave turbulence：梯度变成运动

许多 fusion-relevant turbulent processes 从 gradients 开始。

Density gradients 和 temperature gradients 含有 free energy。在 magnetized plasma 中，这些 gradients 与 drifts、waves 和 parallel motion 相互作用。

基本 drift-wave intuition 是：

* density 有 gradient；
* perturbations 产生 electric fields；
* electric fields 产生 $E\times B$ motion；
* 这个 motion 搬运 density；
* 被搬运的 density 改变 perturbation。

$E\times B$ velocity 是：

$$
\mathbf{v}_E
=
\frac{\mathbf{E}\times\mathbf{B}}{B^2}
$$

它对 ions 和 electrons 相同，因此可以在不立刻分离电荷的情况下跨磁场搬运 plasma。

这使它成为非常有效的 transport mechanism。

Turbulence 常常表现为 fluctuating electric fields 产生 fluctuating $E\times B$ flows。这些 flows 把 density 和 temperature 搅过 magnetic surfaces。

结果不是单个粒子靠碰撞的 simple diffusion。

它是 collective cross-field mixing。

---

## 5. Turbulent transport：来自 correlations 的 flux

Turbulent flux 常常是 fluctuating quantity 与 fluctuating velocity 的 correlation。

Particle transport：

$$
\Gamma_r
=
\langle \tilde{n}\,\tilde{v}_r\rangle
$$

Heat transport 也类似，用 temperature 或 pressure fluctuations：

$$
Q_r
\sim
\langle \tilde{p}\,\tilde{v}_r\rangle
$$

Tilde 表示 fluctuation。Brackets 表示 average。

这是一个微妙点。

只有 fluctuation 还不够。

如果 density fluctuations 和 radial velocity fluctuations 失相，平均 transport 可能很小。如果它们相关，turbulence 就产生净 flux。

所以 plasma turbulence 不是“随机运动”。

它是带有 correlations、能够搬运粒子和热量的 organized randomness。

---

## 6. Cascade：能量跨尺度移动

普通流体湍流中，energy 可以从大尺度 cascade 到小尺度。

Plasma turbulence 也 cascade，但多了额外通道：waves、particles、fields、magnetic geometry 和 velocity space。

Energy 可以移动：

* 从 equilibrium gradients 进入 unstable modes；
* 从 unstable modes 进入其他 modes；
* 通过 resonances 从 fields 进入 particles；
* 从 large eddies 到 small eddies；
* 从 real space 进入 velocity-space structure；
* 从 turbulence 进入 zonal flows。

这就是为什么 plasma turbulence 不像一个现象，而像一座相互作用的城市。

Cascade 不只是耗散能量。

它重新分配 free energy，直到 plasma 在 drive 和 damping 之间找到 nonlinear balance。

---

## 7. Zonal flows：turbulence 创造自己的调节器

Magnetized plasma 中一个重要 nonlinear surprise 是 zonal flow。

Zonal flows 是大尺度、带状的 $E\times B$ flows，主要沿跨磁场方向变化。它们可以 shear apart turbulent eddies。

这创造了 feedback loop：

* gradients 驱动 turbulence；
* turbulence 驱动 zonal flows；
* zonal flows shear turbulence；
* reduced turbulence 改变 transport；
* changed transport 重塑 gradients。

这是 plasma 在调节自己。

它不是简单 stability。
也不是简单 instability。

它是 nonlinear self-organization。

在 fusion 中，这很重要，因为 confinement regimes 可能取决于 shear flows 是否有效抑制 turbulence。著名的 improved confinement transition 就与这个更广泛的想法有关：flows 可以调节 turbulent transport。

Plasma 不只是在泄漏。

它有时也在建造减少泄漏的结构。

---

## 8. Magnetic reconnection：nonlinear topology change

并非所有 nonlinear plasma behavior 都是 drift-wave turbulence。

Magnetic reconnection 是另一个主要例子。

在 ideal MHD 中，磁力线 frozen into plasma。Topology 被保存。

有 finite resistivity 或 kinetic effects 时，field lines 可以断开并重新连接。Magnetic energy 可以转化为 particle energy、flows 和 heat。

Reconnection 在 solar flares、magnetospheres、laboratory plasmas 和 fusion devices 中都重要。

在 confinement devices 中，tearing modes 与 reconnection 有关。Magnetic islands 可以形成。如果 islands 足够大，会降低 confinement。如果多个 islands overlap，field lines 可以变成 stochastic，形成快速 transport paths。

这之所以 nonlinear，是因为 instability 改变了控制 instability 的 magnetic geometry。

地图在旅行者行走时重画自己。

---

## 9. 为什么 turbulence 难以预测

Turbulence 难，是因为它 sensitive、multiscale、self-consistent。

它依赖：

* equilibrium profiles；
* magnetic geometry；
* gradients；
* collisions；
* trapped particles；
* finite Larmor radius effects；
* wave-particle resonances；
* boundary conditions；
* flows and shear；
* impurities and radiation。

一个层面的微小变化可以改变另一个层面。

Profile change 可以改变 instability。
Instability 可以改变 transport。
Transport 可以改变 profile。
改变后的 profile 可以 stabilize 或 destabilize 另一个 mode。

所以 fusion modeling 不能只是 local 和 linear。

Plasma 是 feedback system。

它必须被当作 feedback system 建模。

---

## 10. 简单模型仍然重要

如果 turbulence 会打破简单模型，为什么还要学简单模型？

因为简单模型告诉我们该看什么。

Single-particle theory 告诉我们 orbit scales。
Fluid theory 告诉我们 conservation laws。
MHD 告诉我们 large-scale force balance。
Transport theory 告诉我们 confinement time。
Kinetic theory 告诉我们 resonances 和 velocity-space drives。

Turbulence 不会抹掉这些层。

它把它们纠缠在一起。

好的 plasma intuition 来自知道哪个简单模型正在被打破，以及如何被打破。

失效方式本身就是信息。

---

## 11. 为什么这对 fusion 和 stellarators 重要

Fusion devices 围绕 confinement 设计。

但 confinement 常常受到 turbulent transport 限制。

对 tokamaks 来说，turbulence 帮助决定 energy confinement、pedestal behavior、profile stiffness 和 operational limits。

对 stellarators 来说，turbulence 必须与 neoclassical transport 和三维几何一起考虑。为一种 loss channel 优化的几何，不一定自动最小化另一种损失。好的 stellarator design 越来越意味着平衡 MHD stability、neoclassical confinement、turbulent transport、coil feasibility 和 engineering constraints。

这就是 plasma physics 变成 nonlinear uncertainty 下的 design。

问题不只是：

> 这个 configuration 稳定吗？

而是：

> 所有相关 instabilities 饱和之后，它会产生什么 transport？

这难得多。

也更接近 reactor problem。

---

## 结尾

Linear theory 告诉我们扰动什么时候开始增长。

Nonlinear theory 告诉我们扰动增长后 plasma 变成什么。

Turbulence 是 free energy、fields、particles 和 geometry 相互 feedback 后产生的 collective、multiscale consequence。

它解释了为什么 confinement 很少像最干净的理论预测那样好。

也解释了为什么 plasma 如此鲜活。

系统不只是在失去能量。
它在组织、破裂、调节和重新排列自己。

简单模型仍然必要。

但 turbulence 是 plasma 提醒我们的地方：没有任何单一层次拥有全部真相。
