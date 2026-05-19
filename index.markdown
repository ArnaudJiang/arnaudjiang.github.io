---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: landing
---

<figure style="margin: 0 0 1.5rem 0;">
  <img
    src="{{ "/assets/images/home-portrait.jpg" | relative_url }}"
    alt="Arnaud Jiang in a playground"
    width="480"
    height="480"
    style="display: block; width: min(100%, 220px); height: auto; border-radius: 8px;"
  >
</figure>

## Research Series

- [Plasma & Fusion]({{ "/plasma-fusion/" | relative_url }}) / [中文]({{ "/zh/plasma-fusion/" | relative_url }})  
  A layered reconstruction of plasma physics: from collective charged matter, to computational models, to magnetic fusion and stellarator design.

## Latest Posts

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | normalize_whitespace | truncate: 220 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
