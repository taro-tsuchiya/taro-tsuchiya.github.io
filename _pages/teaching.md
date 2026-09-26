---
layout: page
permalink: /teaching/
title: teaching
description:
nav: true
nav_order: 5
---

{% for group in site.data.teaching.Teaching %}
<p class="mt-3 mb-1">
  <strong>{{ group.role }}</strong>{% if group.institution %} @ {{ group.institution }}{% endif %}{% if group.date %} <span class="text-muted">({{ group.date }})</span>{% endif %}
</p>
{% if group.items.size > 0 %}
<ul class="mb-2">
{% for item in group.items %}
  <li>{{ item.text }} <span class="text-muted">({{ item.date }})</span></li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}
