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

This is the top-level map for my notes on plasma physics, magnetic fusion, simulation, and stellarator thinking.

<p><strong>Language:</strong> English | <a href="{{ "/zh/plasma-fusion/" | relative_url }}">中文</a></p>

> A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design.

## Start Here

1. [Plasma & Fusion: Overview]({{ "/plasma-fusion/overview/" | relative_url }}) / [中文]({{ "/zh/plasma-fusion/overview/" | relative_url }})  
   What this series is, why I am writing it, and how it is organized.
2. [Origin: Why Plasma & Fusion]({{ "/plasma-fusion/origin/" | relative_url }}) / [中文]({{ "/zh/plasma-fusion/origin/" | relative_url }})  
   A research motivation statement for energy, mobility, computation, and plasma control.

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
