---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
{% for group in site.data.publications %}
<h4 class="mt-4 mb-2 pb-1" style="border-bottom: 1px solid var(--global-theme-color);">{{ group.section }}</h4>
{% for item in group.items %}
<div class="mb-3">
  <div>{% if item.venue %}<strong>[{{ item.venue }}]</strong> {% endif %}{{ item.title }}</div>
  <div class="pl-3"><small>
    {%- for author in item.authors -%}
      {%- if author contains "Tsuchiya" -%}<u>{{ author }}</u>{%- else -%}{{ author }}{%- endif -%}
      {%- unless forloop.last %}, {% endunless -%}
    {%- endfor -%}
    {% if item.note %}<br>{{ item.note }}{% endif %}
    {% if item.detail %}<br>{{ item.detail }}{% endif %}
    <br>{% for link in item.links %}[<a href="{% if link.url contains '://' %}{{ link.url }}{% else %}{{ link.url | relative_url }}{% endif %}" target="_blank">{{ link.label }}</a>] {% endfor %}
  </small></div>
</div>
{% endfor %}
{% endfor %}

<div class="mt-5"></div>

## Media Coverage

<p class="text-muted"><small>{{ site.data.media.intro }}</small></p>

<ul class="mb-2">
{% for item in site.data.media.items %}
  <li><a href="{{ item.url }}" target="_blank">{{ item.outlet }}</a> &ldquo;{{ item.headline }}&rdquo;</li>
{% endfor %}
</ul>
