---
layout: page
title: "Plasma & Fusion"
permalink: /plasma-fusion/
lang: en
alternate_lang: zh
alternate_url: /zh/plasma-fusion/
series: plasma-fusion
series_layer: hub
series_order: 0
description: "A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design."
---

This is the top-level map for my notes on plasma physics and nuclear fusion.

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/" | relative_url }}">中文</a></p>

I studied physics, but I am approaching this topic again from a new position: with more engineering experience, more exposure to AI systems, and a stronger interest in simulation, computation, and applied scientific infrastructure. Plasma and fusion sit at an unusual intersection of theory, experiment, control, materials, numerical methods, and large-scale engineering. That makes the field difficult, but also unusually rich.

> A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design.

## Start Here

- [Plasma & Fusion: Overview]({{ "/plasma-fusion/overview/" | relative_url }})  
  The first published note for this research series.
- [Origin: Why Plasma & Fusion]({{ "/plasma-fusion/origin/" | relative_url }}) / [中文]({{ "/zh/plasma-fusion/origin/" | relative_url }})  
  A research motivation statement for energy, mobility, computation, and plasma control.

## Series Structure

The series has three layers. They are not simply "easy, medium, hard." They are organized by cognitive scale.

| Layer | Main task | Writing style | Formula density |
| --- | --- | --- | --- |
| Origin | Explain the motivation | Personal research note | Very low |
| Conceptual | Build physical intuition | Images, analogies, simple diagrams | Low |
| Modeling | Build the model stack | Approximation, tradeoff, equation meaning | Medium |
| Fusion / Stellarator | Connect physics to devices | Physics to device to engineering | Medium-low |

## Series Map

{% for layer in site.data.plasma_fusion.layers %}
### {{ layer.title_en }}

{{ layer.description_en }}

<ul>
{% for item in layer.items %}
  <li>
    <strong>
      {% if item.status == "Published" and item.url_en %}
        <a href="{{ item.url_en | relative_url }}">{{ item.title_en }}</a>
      {% else %}
        {{ item.title_en }}
      {% endif %}
    </strong><br>
    {{ item.description_en }}<br>
    <small>
      {% if item.status == "Published" and item.url_en %}
        <a href="{{ item.url_en | relative_url }}">English</a>{% if item.url_zh %} | <a href="{{ item.url_zh | relative_url }}">中文</a>{% endif %} ·
      {% endif %}
      Status: {{ item.status }}
    </small>
  </li>
{% endfor %}
</ul>
{% endfor %}

## Writing Workflow

The source files remain ordinary Markdown posts. English posts in this series live under `_posts/plasma-fusion/`, keep stable `/plasma-fusion/.../` permalinks, and continue to appear in the blog's post feed.
