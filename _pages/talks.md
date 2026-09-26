---
layout: page
permalink: /talks/
title: talks
description: Conference presentations and invited talks.
nav: true
nav_order: 4
---

{% for group in site.data.talks %}
<p class="mt-3 mb-1"><strong>&ldquo;{{ group.title }}&rdquo;</strong></p>
<ul class="mb-2">
{% for item in group.items %}
  <li>{{ item.detail }} <span class="text-muted">({{ item.date }})</span></li>
{% endfor %}
</ul>
{% endfor %}
