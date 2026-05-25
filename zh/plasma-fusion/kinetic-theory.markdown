---
layout: page
title: "Kinetic Theory：当平均量不够用"
permalink: /zh/plasma-fusion/kinetic-theory/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/kinetic-theory/
series: plasma-fusion
series_layer: modeling
series_order: 10
description: "分布函数、Landau damping 和波粒相互作用。"
excerpt: "分布函数、Landau damping 和波粒相互作用。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/kinetic-theory/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Kinetic Theory：当平均量不够用

*分布函数、Landau damping 和波粒相互作用*

Fluid models 强大，是因为它们会遗忘。

它们用 density、velocity、pressure 和 temperature 替代许多粒子。MHD 甚至遗忘更多：把 ion 和 electron behavior 压缩成一种 conducting fluid。

这种遗忘很有用。

但 plasma 对 fluid 隐藏的细节有很长的记忆。

有时 velocity distribution 的精确形状很重要。有时一小群 resonant particles 决定一个波增长还是阻尼。有时 pressure 在不同方向并不相同。有时最高能粒子的行为不同于 bulk。

这些都是 kinetic problems。

Kinetic theory 从 averages 不够用的地方开始。

---

## 1. Kinetic theory 的对象：distribution function

Kinetic theory 不只问位置 $\mathbf{x}$ 处的 density，而是问粒子如何同时分布在 position 和 velocity 中。

核心对象是 distribution function：

$$
f_s(\mathbf{x},\mathbf{v},t)
$$

对 species $s$ 来说，它表示：

> 在时间 $t$，有多少粒子位于 $\mathbf{x}$ 附近，并且速度位于 $\mathbf{v}$ 附近？

Density 通过对 velocity 积分得到：

$$
n_s(\mathbf{x},t) = \int f_s(\mathbf{x},\mathbf{v},t)\,d^3v
$$

Bulk velocity 是 velocity average：

$$
\mathbf{u}_s(\mathbf{x},t)
=
\frac{1}{n_s}
\int \mathbf{v} f_s(\mathbf{x},\mathbf{v},t)\,d^3v
$$

Pressure 和 temperature 来自围绕平均速度的 spread。

关键关系是：

Fluid variables 是 distribution function 的 moments。

Fluid theory 看见影子。
Kinetic theory 研究投下影子的对象。

---

## 2. Phase space：plasma 活在六维里

普通空间有三维。

Kinetic theory 加上三维速度。

组合空间叫 phase space：

$$
(\mathbf{x},\mathbf{v})
$$

Plasma distribution 在这个六维空间中演化。

这就是 kinetic theory 昂贵的原因。即使还没加上时间、场、碰撞和边界，基本未知量已经比 fluid theory 大得多。

但回报也巨大。

Velocity space 包含 density field 无法表达的物理：

* fast particles；
* trapped particles；
* beams；
* rings；
* loss cones；
* temperature anisotropy；
* resonant particles；
* non-Maxwellian tails。

这些不是装饰性细节。

在 plasma 中，它们可以驱动波、阻尼波、携带电流、触发 modes，并决定 heating efficiency。

Velocity distribution 不是记账。
它是动力学来源。

---

## 3. Vlasov equation：无碰撞演化

许多 plasma 中，碰撞太少，不是主要组织力量。

无碰撞 kinetic equation 是 Vlasov equation：

$$
\frac{\partial f_s}{\partial t}
+
\mathbf{v}\cdot\nabla_{\mathbf{x}} f_s
+
\frac{q_s}{m_s}
\left(
\mathbf{E}+\mathbf{v}\times\mathbf{B}
\right)
\cdot\nabla_{\mathbf{v}} f_s
=0
$$

第一项是时间演化。

第二项让粒子穿过物理空间。

第三项让粒子在 Lorentz force 作用下穿过 velocity space。

与 Maxwell's equations 耦合后，它变成 Vlasov-Maxwell system。

概念上，它说：

> distribution 产生 charge 和 current；charge 和 current 产生 fields；fields 推动 distribution 在 phase space 中运动。

这就是 plasma self-consistency 的 kinetic version。

很美。
也很残酷。

---

## 4. Collisions 和 Boltzmann picture

真实 plasma 并不总是 collisionless。

当碰撞重要时，kinetic equation 会多一个 collision operator：

$$
\frac{\partial f_s}{\partial t}
+
\mathbf{v}\cdot\nabla_{\mathbf{x}} f_s
+
\frac{q_s}{m_s}
\left(
\mathbf{E}+\mathbf{v}\times\mathbf{B}
\right)
\cdot\nabla_{\mathbf{v}} f_s
=
\left(\frac{\partial f_s}{\partial t}\right)_{\mathrm{coll}}
$$

Collision term 是 relaxation、resistivity、thermalization 和 transport 进入的地方。

但 Coulomb collisions 很微妙。它们是 long-range 的。Plasma 粒子通常不是发生少数 hard-sphere impacts，而是经历许多 small-angle deflections。

这让 plasma kinetic theory 不同于普通 gas kinetic theory。

Collisions 会缓慢把 distributions 推向 Maxwellians，但 waves 和 fields 会不断把它们拉开。

Plasma 常常悬在 relaxation 和 drive 之间。

---

## 5. Maxwellian 是平静状态

Maxwellian distribution 是熟悉的热平衡形状：

$$
f_M(\mathbf{v})
=
n
\left(
\frac{m}{2\pi k_B T}
\right)^{3/2}
\exp\left[
-\frac{m|\mathbf{v}-\mathbf{u}|^2}{2k_B T}
\right]
$$

它由 density $n$、bulk velocity $\mathbf{u}$ 和 temperature $T$ 描述。

这就是为什么 fluid theory 常常有效：如果 distribution 足够接近 Maxwellian，少数 moments 就能捕捉很多故事。

但“close” 这个词很危险。

一个 distribution 可能看起来几乎 Maxwellian，却有一个 resonant tail 控制 wave damping。
一小群 energetic particles 可以 destabilize Alfvén mode。
Anisotropic temperature 可以触发 mirror 或 firehose instabilities。
Loss cone 可以在 mirror machine 中驱动 waves。

Bulk 也许平静，但 tail 正在和 fields 谈判。

Fluid theory 把这场谈判平均掉。

Kinetic theory 听见它。

---

## 6. Landau damping：没有碰撞的阻尼

Landau damping 是 kinetic theory 存在的最重要原因之一。

普通 fluid 中，damping 常常来自 viscosity 或 collisions。

在 collisionless plasma 中，wave 仍然可以 damp。

怎么做到？

速度接近 wave phase velocity 的粒子可以与波交换能量。Wave 的 phase velocity 是：

$$
v_\phi = \frac{\omega}{k}
$$

速度接近 $v_\phi$ 的粒子能与波保持足够久的相位关系，从而获得或失去能量。

如果比波稍慢的粒子略多于比波稍快的粒子，波就把能量给粒子并被阻尼。对 Maxwellian distribution 来说，这通常成立，因为 $f(v)$ 随速度增大而下降。

结果是没有 binary collisions 的 damping。

这非常 non-fluid。

Fluid model 可以知道 density 和 pressure，却仍然错过 $v_\phi$ 处 $f(v)$ 的 resonant slope。

Landau damping 说：

> resonant velocity 处 distribution function 的导数，可以决定一个波的命运。

这就是 kinetic thinking。

---

## 7. Wave-particle interaction

Plasma waves 不只是穿过被动介质的 fields。

它们在和粒子对话。

当粒子能与波保持一致相位关系时，就发生 resonance。基本 electrostatic resonance 是：

$$
\omega - k_\parallel v_\parallel = 0
$$

在 magnetized plasmas 中，还会出现 cyclotron harmonics：

$$
\omega - k_\parallel v_\parallel = n\Omega_s
$$

其中 $\Omega_s$ 是 gyrofrequency，$n$ 是整数。

这些 resonances 是 heating 和 instability 的核心。

Radio-frequency heating 用 waves 把能量沉积到选定粒子群中。Energetic particles 可以把能量喂给 Alfvén waves。Drift waves 可以与沿磁力线运动的粒子交换能量。

在 kinetic theory 中，wave 不只是 mode。

它是 energy exchange channel。

---

## 8. 当 pressure 变成 tensor

Fluid equations 常用 scalar pressure：

$$
p = nk_B T
$$

但 kinetic theory 说明它为什么会失败。

在 magnetized plasma 中，平行和垂直于磁场的运动并不等价。Distribution 可能有：

$$
T_\parallel \neq T_\perp
$$

这时 pressure 不是一个数，而是 anisotropic：

$$
p_\parallel = nk_B T_\parallel,
\quad
p_\perp = nk_B T_\perp
$$

更一般地，pressure 是 tensor：

$$
\mathsf{P}
=
m\int
(\mathbf{v}-\mathbf{u})(\mathbf{v}-\mathbf{u})
f\,d^3v
$$

这很重要，因为 pressure anisotropy 可以驱动 instabilities。

例如，过多 perpendicular pressure 可以产生 mirror-like behavior。过多 parallel pressure 可以产生 firehose-like behavior。

Plasma 不只是有“一个温度”。

它有 velocity-space shape。

---

## 9. Kinetic theory 和 transport

上一篇文章把 transport 描述成粒子和热量的慢泄漏。

Kinetic theory 解释为什么 transport 比 simple diffusion 丰富得多。

粒子可以被 magnetic mirrors 困住。
Trapped particles 可以径向漂移。
Collisions 可以把粒子散射进 loss regions。
Waves 可以只与某些速度共振。
Turbulence 可以造成 stochastic orbits。

Neoclassical transport 已经部分是 kinetic 的，因为它依赖 toroidal geometry 中的粒子轨道。

Turbulent transport 常常也是 kinetic 的，因为 instability drive 依赖 gradients、resonances、finite Larmor radius effects 和 trapped particles。

所以 kinetic theory 不是 fluid theory 后面的装饰层。

当 transport 取决于粒子是谁，而不只是粒子有多少时，就需要 kinetic theory。

---

## 10. 为什么 kinetic theory 对 fusion 重要

Fusion plasmas 充满 kinetic questions。

Heating：

> 哪些粒子吸收 wave power？

Alpha particles：

> 高能 fusion products 能否被约束足够久来加热 plasma？

Instability：

> Fast ions 会不会驱动 Alfvén eigenmodes？

Transport：

> 哪些 microinstabilities 把热量跨磁力线搬走？

Edge physics：

> 粒子如何与 sheaths、neutrals 和 material boundaries 相互作用？

Current drive：

> Waves 能否推动 electron distribution 来维持 current？

每个问题都依赖 velocity-space structure。

MHD 可以告诉我们大尺度 magnetic-fluid structure 能否存在。

Kinetic theory 问的是：这个结构里的粒子是否足够听话。

---

## 11. 不做平均的代价

Kinetic theory 更准确，但不是免费的。

未知量活在 phase space 中。六维加时间，非常昂贵。

因此实际 plasma modeling 使用许多 reduced kinetic models：

* drift-kinetic theory；
* gyrokinetic theory；
* bounce-averaged kinetic theory；
* Fokker-Planck solvers；
* particle-in-cell simulation。

每一种都保留部分 kinetic truth，同时丢掉部分过快或不必要的细节。

对 magnetized fusion plasmas 来说，gyrokinetics 尤其重要，因为它平均掉快速 gyromotion，同时保留驱动 turbulence 和 transport 的慢 drift 与 wave-particle physics。

熟悉的模式又出现了：

Plasma physics 通过选择遗忘什么来前进。

Kinetic theory 比 fluid theory 遗忘得少。
但即使 kinetic theory 也必须遗忘一些东西，才可计算。

---

## 结尾

Fluid theory 询问 density、velocity、pressure 和 temperature。

Kinetic theory 询问 distribution function。

这个转变打开了 velocity space。

它揭示 resonant particles、anisotropy、trapped orbits、non-Maxwellian tails 和 collisionless damping。

它解释了 wave 如何在没有 collisions 的情况下失去能量。
它解释了一小群粒子如何控制一个大 mode。
它解释了为什么 transport 常常拒绝成为简单 diffusion coefficient。

当 averages 足够时，fluid theory 很美。

当 $f(\mathbf{x},\mathbf{v},t)$ 的形状重要时，kinetic theory 开始。
