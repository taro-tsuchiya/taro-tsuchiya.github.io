---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{% bibliography -f {{ site.scholar.bibliography }} %}

</div>

<div class="mt-5"></div>

## Media Coverage

<p class="text-muted"><small>{{ site.data.media.intro }}</small></p>

<ul class="mb-2">
{% for item in site.data.media.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.outlet }}</a> &ldquo;{{ item.headline }}&rdquo;</li>
{% endfor %}
</ul>
