---
layout: page
title: "Plasma & Fusion"
permalink: /zh/plasma-fusion/
lang: zh
alternate_lang: en
alternate_url: /plasma-fusion/
series: plasma-fusion
series_layer: hub
series_order: 0
description: "从带电物质的集体行为出发，经由计算模型，走向磁约束聚变与仿星器设计。"
---

这是我关于等离子体物理、磁约束聚变、仿真与仿星器思维的顶层地图。

<p><strong>语言：</strong><a href="{{ "/plasma-fusion/" | relative_url }}">English</a> | 中文</p>

> 从带电物质的集体行为出发，经由计算模型，走向磁约束聚变与仿星器设计。

## 从这里开始

1. [Plasma & Fusion：概览]({{ "/zh/plasma-fusion/overview/" | relative_url }}) / [English]({{ "/plasma-fusion/overview/" | relative_url }})  
   这个系列是什么、为什么要写、以及它会如何组织。
2. [Origin：为什么关注 Plasma & Fusion]({{ "/zh/plasma-fusion/origin/" | relative_url }}) / [English]({{ "/plasma-fusion/origin/" | relative_url }})  
   一份关于能源、移动性、计算和等离子体控制的研究动机声明。

## Series Map

{% for layer in site.data.plasma_fusion.layers %}
### {{ layer.title_zh }}

{{ layer.description_zh }}

<ul>
{% for item in layer.items %}
  <li>
    <strong>
      {% if item.status == "Published" and item.url_zh %}
        <a href="{{ item.url_zh | relative_url }}">{{ item.title_zh }}</a>
      {% else %}
        {{ item.title_zh }}
      {% endif %}
    </strong><br>
    {{ item.description_zh }}<br>
    <small>
      {% if item.status == "Published" and item.url_zh %}
        <a href="{{ item.url_zh | relative_url }}">中文</a>{% if item.url_en %} | <a href="{{ item.url_en | relative_url }}">English</a>{% endif %} ·
      {% endif %}
      状态：{{ item.status_zh }}
    </small>
  </li>
{% endfor %}
</ul>
{% endfor %}

## 结语

这个系列从 plasma 作为带电物质的集体行为开始，最后落到 fusion 作为耦合设计问题。它有意按层推进：先是粒子与场，然后是流体和 kinetic models，再到 transport、turbulence、magnetic confinement，以及 stellarator geometry。

核心教训是：fusion 不是一个单独问题。它是一串近似和约束：physics 变成 modeling，modeling 变成 geometry，geometry 变成 engineering，而每一层又都会反过来影响 plasma。

这就是 plasma 为什么难，也正是它值得认真学习的原因。
