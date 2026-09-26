---
layout: page
permalink: /service/
title: service
description:
nav: true
nav_order: 6
---

{% for group in site.data.teaching.Service %}
<p class="mt-3 mb-1"><strong>{{ group.role }}</strong></p>
<ul class="mb-2">
{% for item in group.items %}
  <li>{{ item.text }} <span class="text-muted">({{ item.date }})</span></li>
{% endfor %}
</ul>
{% endfor %}
