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

## 写作工作流

英文源文件放在 `_posts/plasma-fusion/`，保持 `/plasma-fusion/.../` 的稳定链接，并继续进入博客发布记录。中文内容集中放在 `zh/plasma-fusion/`。
