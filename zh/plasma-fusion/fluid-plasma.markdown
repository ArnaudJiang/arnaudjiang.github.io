---
layout: page
title: "Fluid Plasma：第一个有用近似"
permalink: /zh/plasma-fusion/fluid-plasma/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/fluid-plasma/
series: plasma-fusion
series_layer: modeling
series_order: 7
description: "continuity、momentum、pressure 和自洽场。"
excerpt: "continuity、momentum、pressure 和自洽场。"
---

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/fluid-plasma/" | relative_url }}">English</a> | 中文</p>

[返回 Plasma & Fusion 系列]({{ "/zh/plasma-fusion/" | relative_url }})

# Fluid Plasma：第一个有用近似

*continuity、momentum、pressure 和自洽场*

等离子体由粒子组成，但等离子体物理不能长期停留在逐个粒子的故事里。

在前一层中，我们看的是带电粒子在给定电场和磁场中的运动。那已经足够丰富：Larmor motion、guiding center、$E \times B$ drift、grad-$B$ drift、curvature drift、magnetic mirror。但背景中藏着一个人为简化：

场是给定的。

真实等离子体不会乖乖地在别人准备好的场里运动。粒子产生电荷密度和电流。电荷密度和电流产生电场和磁场。这些场又推动粒子。运动和场必须一起求解。

这就是等离子体物理的自洽问题。Chen 直接描述了这个困难：在等离子体中，$E$ 和 $B$ 不是预先给定的；它们由电荷自身的位置和运动决定。我们必须找到彼此一致的粒子运动和场结构，让二者相互生成。他也指出为什么完全微观的路线是无望的：一个典型等离子体每立方米可能包含大约 $10^{18}$ 对离子和电子，所以逐个跟踪所有轨道并不是第一个有用策略。令人意外的是，一个粗糙的流体模型就能解释大量观测到的等离子体现象。

这就是流体近似的意义。

这是等离子体物理第一次从“许多带电粒子”变成“运动的带电物质”。

---

## 1. 把等离子体当作流体是什么意思？

流体描述会丢掉单个粒子的身份。

它不再问：

> 这个电子在哪里？它的速度是多少？它沿着什么轨道运动？

它问的是：

> 在空间中的这一点，密度是多少？平均速度是多少？压强是多少？这里存在什么电场和磁场？

对每一种粒子，通常是离子和电子，我们引入这些场：

$$
n_s(\mathbf{x},t)
$$

species $s$ 的密度，

$$
\mathbf{v}_s(\mathbf{x},t)
$$

整体流体速度，

$$
p_s(\mathbf{x},t)
$$

压强，

然后把它们耦合到

$$
\mathbf{E}(\mathbf{x},t), \quad \mathbf{B}(\mathbf{x},t)
$$

也就是电磁场。

“流体”这个词可能有一点误导。它不是说等离子体在每个方向上都像水。它说的是，我们对许多粒子取平均，只描述 coarse-grained fields。

水分子主要通过碰撞被拖进流体行为。等离子体更奇怪。它可以是弱碰撞的，但在很多情况下仍然表现得像流体，因为磁场限制了沿垂直于磁场方向的自由流动。带电粒子不能简单地在横跨磁场的方向上一直加速；它会回旋。从这个意义上说，磁场可以部分替代普通流体中由碰撞承担的组织作用。Chen 明确指出，流体图像对垂直于 $B$ 的运动尤其有效，而沿 $B$ 的运动更容易暴露 kinetic effects。

所以流体近似并不是说：

> 粒子不重要。

它说的是：

> 对许多大尺度问题，平均运动首先重要。

---

## 2. Continuity equation：等离子体不会随便消失

第一个流体方程是记账。

如果一个区域内的密度发生变化，要么粒子流入了，要么粒子流出了，要么粒子被创造或湮灭了。暂时忽略源项和汇项，粒子数守恒给出：

$$
\frac{\partial n_s}{\partial t}+\nabla\cdot(n_s\mathbf{v}_s)=0
$$

这就是 continuity equation。

它说：

* $n_s$ 会随时间变化，如果存在净通量不平衡。
* $n_s\mathbf{v}_s$ 是粒子通量。
* $\nabla\cdot(n_s\mathbf{v}_s)$ 衡量粒子是在散开还是汇聚。

对等离子体来说，这个方程对每一种粒子分别存在：

$$
\frac{\partial n_i}{\partial t}+\nabla\cdot(n_i\mathbf{v}_i)=0
$$

$$
\frac{\partial n_e}{\partial t}+\nabla\cdot(n_e\mathbf{v}_e)=0
$$

这已经不同于中性气体。离子和电子可以以不同方式运动。如果它们哪怕只是轻微分离，就会产生电荷不平衡。电荷不平衡产生电场。电场再把它们推回去、拉开，或者驱动波。

这就是为什么在等离子体中，密度不只是密度。

密度也可能是场的来源。

Chen 从物质守恒推导 continuity equation：一个体积中的粒子数只能通过边界上的净粒子通量改变。局域形式正是上面的方程；如果需要，也可以加入源项或汇项。

---

## 3. Momentum equation：带电流体的 Newton 定律

第二个核心方程是 Newton 定律的流体版本。

对单个粒子，我们知道：

$$
m\frac{d\mathbf{v}}{dt}=q(\mathbf{E}+\mathbf{v}\times\mathbf{B})
$$

对一个流体 species，对应方程变成：

$$
m_s n_s
\left(
\frac{\partial \mathbf{v}_s}{\partial t}
+
\mathbf{v}_s\cdot\nabla \mathbf{v}_s
\right)
=
q_s n_s(\mathbf{E}+\mathbf{v}_s\times\mathbf{B})
-\nabla p_s
$$

这是基本的等离子体流体 momentum equation。

左边是惯性。右边有两种主要力：

$$
q_s n_s(\mathbf{E}+\mathbf{v}_s\times\mathbf{B})
$$

电磁力密度，

以及

$$
-\nabla p_s
$$

压强梯度力。

这个方程是从单粒子等离子体物理通向集体等离子体动力学的概念桥梁。

单粒子理论说：

> 一个带电粒子会回旋和漂移。

流体理论说：

> 整个带电 species 会加速、压缩、膨胀、漂移，通过压强反推，并产生场。

Chen 通过在平均运动方程中加入压强，并推广到三维，推导出流体方程。在各向同性情形中，压强力表现为 $-\nabla p$。在更一般的情况下，标量压强必须被 stress tensor 取代。

---

## 4. Convective derivative：为什么流体加速度不只是 $\partial/\partial t$

这一项

$$
\frac{\partial \mathbf{v}}{\partial t}
+
\mathbf{v}\cdot\nabla\mathbf{v}
$$

很容易被低估。

它叫 convective derivative。

第一部分，

$$
\frac{\partial \mathbf{v}}{\partial t}
$$

表示固定空间点上的速度随时间变化。

第二部分，

$$
\mathbf{v}\cdot\nabla\mathbf{v}
$$

表示一个流体元运动到速度场不同的区域。

一条河可以在时间上保持稳定，但一艘顺流而下的小船仍然可能加速，如果河道变窄、流速增加。局部流场没有随时间变化，但运动中的物体经历了变化。

这就是 convective term 捕捉的东西。

等离子体需要它，因为我们不再跟踪一个粒子。我们跟踪定义在空间点上的场。一个流体元穿过这些场，导数必须同时知道“这里随时间怎么变”和“沿着运动方向空间上怎么变”。

这一项也是流体等离子体第一次变成 nonlinear 的地方。速度场乘上自己的梯度。许多初等波动计算后来会通过线性化丢掉这一项，但它一直在背景中等待，让系统重新变成非线性。

---

## 5. Pressure：热运动重新变成一种力

等离子体中的压强不是装饰。它是微观随机运动在宏观模型中重新出现的方式。

一个流体元包含许多粒子。即使整体速度是 $\mathbf{v}_s$，单个粒子仍然围绕这个平均速度具有随机热速度。进入一个小体积的粒子可能从一侧多于另一侧。某个方向携带的动量也可能多于另一个方向。结果就是压强力。

对各向同性等离子体，

$$
p_s = n_s K T_s
$$

其中 $K$ 是 Boltzmann constant。

然后压强会从高压区域推向低压区域：

$$
-\nabla p_s
$$

这一项负责 sound wave、ion acoustic wave、diffusion、diamagnetic drift，以及等离子体许多“流体性格”。

但等离子体压强比普通气体压强更微妙。在磁场中，平行和垂直于 $B$ 的运动并不等价。一个 species 可以有

$$
T_\parallel \neq T_\perp
$$

所以压强可能变成各向异性：

$$
p_\parallel = nKT_\parallel
$$

$$
p_\perp = nKT_\perp
$$

这时压强不再能由一个标量完全表示。它会变成 stress tensor。Chen 给出各向同性压强张量时，它在所有方向上以 $p$ 作为对角项；而磁化各向异性版本则在两个垂直方向上使用 $p_\perp$，沿磁场方向使用 $p_\parallel$。

这对磁约束非常重要。

Tokamak 或 stellarator 约束的并不是简单的“热气体”。它约束的是一种磁化介质：压强可能依赖方向，电流会改变场，场几何又会改变压强响应。

这已经是丰富得多的对象了。

---

## 6. Equation of state：闭合模型

到这里我们遇到一个问题。

Continuity equation 演化密度。
Momentum equation 演化速度。
但压强出现在 momentum equation 里。

那么我们怎么知道压强？

我们需要一个 closure relation。

一个简单 closure 是：

$$
p_s = C_s n_s^{\gamma_s}
$$

或者在 isothermal 情况下：

$$
p_s = n_s K T_s
$$

这叫 equation of state。

它告诉流体模型，当密度变化时，压强如何变化。对 isothermal compression，$\gamma=1$。对 adiabatic compression，$\gamma$ 更大。Chen 把这个 closure 作为完成流体系统所需的额外关系。

这不是细枝末节。Closure 是等离子体建模中最深的主题之一。

每次我们把 kinetic system 简化成 fluid system，都是把速度空间信息压缩成几个 moments：密度、平均速度、压强、热流，等等。但每个方程都会引入一个更高阶的量。密度方程需要速度。速度方程需要压强。压强方程会需要热流。热流方程又会需要别的东西。

在某个地方，我们停下来，做一个 closure assumption。

这个停顿不只是数学。它是一个物理赌注。

这个赌注说：

> 未解析的微观行为可以被这个宏观关系足够好地近似。

有时这个赌注非常成功。

有时它会戏剧性地失败。

Landau damping、resonant particles、trapped particles、kinetic instabilities 和 microturbulence 都在提醒我们，速度空间并没有和流体理论签署和平条约。

---

## 7. Self-consistent fields：等离子体不是电磁场里的乘客

现在来到真正让等离子体成为等离子体的部分。

流体方程本身还不够。我们还需要 Maxwell 方程。

在等离子体物理中，通常更适合使用 Maxwell 方程的真空形式，把所有电荷和电流显式包括进去：

$$
\nabla\cdot \mathbf{E} = \frac{\rho}{\epsilon_0}
$$

$$
\nabla\times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t}
$$

$$
\nabla\cdot \mathbf{B}=0
$$

$$
\nabla\times \mathbf{B}
=
\mu_0\mathbf{j}
+
\mu_0\epsilon_0\frac{\partial \mathbf{E}}{\partial t}
$$

电荷密度由各 species 的密度产生：

$$
\rho = \sum_s q_s n_s
$$

对简单的离子-电子等离子体：

$$
\rho = q_i n_i + q_e n_e
$$

电流密度由各 species 的流动产生：

$$
\mathbf{j} = \sum_s q_s n_s \mathbf{v}_s
$$

或者

$$
\mathbf{j}=q_i n_i\mathbf{v}_i+q_e n_e\mathbf{v}_e
$$

这闭合了自洽回路：

$$
(n_s,\mathbf{v}_s,p_s)
\rightarrow
(\rho,\mathbf{j})
\rightarrow
(\mathbf{E},\mathbf{B})
\rightarrow
\text{forces on }(n_s,\mathbf{v}_s,p_s)
$$

这就是流体等离子体的核心。

物质决定场。
场决定物质。
解就是二者之间达成的一致。

Chen 的“完整流体方程组”结合了 Maxwell 方程、各 species 的 momentum equation、continuity equation 和 pressure closure。对 two-species ion-electron plasma，未知量包括 $n_i,n_e,p_i,p_e,\mathbf{v}_i,\mathbf{v}_e,\mathbf{E},\mathbf{B}$，同时求解它们会给出流体近似下的自洽场和运动。

---

## 8. Two-fluid plasma：离子和电子不是同一种流体

初学者常见的一个错误，是把“等离子体流体”想象成一种流体。

但第一个自然的流体模型其实是 two-fluid model：

* ion fluid
* electron fluid

每一种都有自己的密度、速度、压强、电荷和质量。

这很重要，因为电子轻而灵活，离子重而有惯性。电子常常快速响应电场。离子常常携带大部分质量。电子响应和离子响应之间的分离，是许多等离子体波的种子。

对每一种 species：

$$
m_s n_s
\left(
\frac{\partial \mathbf{v}_s}{\partial t}
+
\mathbf{v}_s\cdot\nabla \mathbf{v}_s
\right)
=
q_s n_s(\mathbf{E}+\mathbf{v}_s\times\mathbf{B})
-\nabla p_s
$$

结构相同。

参数不同。

这点不同已经足以生成一个动物园。

Electron plasma wave、ion acoustic wave、drift wave、Alfvén wave、magnetosonic wave——其中许多都可以理解成 two fluids 和 fields 没能完美一起运动的不同方式。

因此 two-fluid picture 不只是一个简化。它是一台生成等离子体现象的机器。

---

## 9. Diamagnetic drift：一种不是粒子漂移的流体漂移

这一章里最漂亮的警告之一是 diamagnetic drift。

从 fluid momentum equation 出发，如果存在横跨磁场的压强梯度，可以得到一个 drift：

$$
\mathbf{v}_{D,s}
=
-\frac{\nabla p_s \times \mathbf{B}}{q_s n_s B^2}
$$

这是由压强梯度造成的流体漂移。

但这并不等于说每个粒子的 guiding center 都以这种方式漂移。事实上，diamagnetic drift 来自这样一个事实：从高密度一侧穿过某个小区域的回旋粒子，比从低密度一侧穿过的更多。流体有一个净流动，即使单个 guiding center 未必有对应的漂移。

这是一个微妙但重要的点。

等离子体流体量是平均量。有些流体效应是许多轨道共同造成的集体记账效应，而不是字面上的单粒子运动。

这就是为什么在粒子直觉和流体直觉之间切换很危险。两者都有用。两者都不拥有全部真相。

对磁约束来说，diamagnetic current 尤其重要，因为压强梯度自然意味着电流，而电流会改变磁场。被约束的等离子体不只是坐在磁瓶里；它正在改变这个瓶子。

小小的背叛。非常等离子体。

---

## 10. 流体近似什么时候有效？

当速度分布的细节不是核心时，流体近似最有效。

它尤其适用于：

* 长度尺度远大于微观轨道尺度；
* 频率低于快速 kinetic timescales；
* 分布足够接近 Maxwellian；
* 压强可以由简单 closure 表示；
* 垂直于磁场的运动占主导；
* wave-particle resonance 不是核心。

它开始失效的情况包括：

* 与波共振的粒子主导能量交换；
* 速度分布强烈非 Maxwellian；
* 温度各向异性变得动力学不稳定；
* heat flux 重要；
* finite Larmor radius effects 重要；
* 碰撞太稀少，不足以支持所选 closure；
* kinetic damping 或 kinetic instability 是主要物理。

这就是为什么 fluid plasma 是第一个有用近似，而不是最终理论。

它捕捉整体编舞。
它会错过一些独奏者。

---

## 11. 为什么这对 fusion 和 stellarator 重要

如果没有流体等离子体，磁约束聚变几乎无法思考。

Stellarator 被设计来产生一种能够约束带电等离子体的磁几何。但等离子体不是被动的。它有压强。它有流动。它有电流。它可以支持波。它可以失稳。它可以扩散。它可以产生电场。它可以改变平衡。

在工程尺度上，人们常常想知道：

* 这个磁构型能否支持一个压强剖面？
* 等离子体会进入什么平衡？
* 密度、压强和电流如何塑造磁场？
* 在扰动下会出现什么波或不稳定性？
* 等离子体如何跨过磁面泄漏？
* 流体模型在哪里失效，kinetic theory 在哪里变得必要？

Fluid plasma 是第一批答案的语言。

之后，MHD 会把离子和电子合并成更接近单一导电流体的对象。Kinetic theory 会重新打开流体理论隐藏起来的速度空间细节。PIC simulation 会在 kinetic reductions 仍然不够时重新回到粒子。

但在这些层次之前，流体近似给了我们第一套可用语法：

$$
\text{continuity} + \text{momentum} + \text{pressure closure} + \text{Maxwell}
$$

这就是第一个 plasma modeling stack。

还不完整。
但终于有用了。

---

## 结尾

单粒子运动教我们，带电粒子如何在给定场中行为。

流体等离子体教我们，当许多这样的粒子变成一种带电介质时会发生什么。

关键转变是自洽性。

等离子体携带密度。
密度和速度产生电荷与电流。
电荷和电流产生场。
场推动等离子体。
压强抵抗压缩。
整个系统在和自己对话。

这场对话，就是真正等离子体物理的开端。
