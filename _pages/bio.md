---
layout: page
permalink: /bio/
title: bio
description:
nav: true
nav_order: 0
---

## Education

{% for edu in site.data.bio.education %}
<p class="mt-3 mb-1">
  <strong>{{ edu.institution }}</strong>{% if edu.degree %}, <em>{{ edu.degree }}</em>{% endif %}
  {% if edu.date %} <span class="text-muted">({{ edu.date }})</span>{% endif %}
</p>
{% if edu.details.size > 0 %}
<ul class="mb-2">
{% for line in edu.details %}
  <li>{{ line }}</li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

<div class="mt-5"></div>

## Experience

{% for exp in site.data.bio.experience %}
<p class="mt-3 mb-1">
  <strong>{{ exp.role }}</strong> @ {{ exp.institution }}{% if exp.extra %}, {{ exp.extra }}{% endif %}
  {% if exp.date %} <span class="text-muted">({{ exp.date }})</span>{% endif %}
</p>
{% if exp.items.size > 0 %}
<ul class="mb-2">
{% for item in exp.items %}
  <li>{{ item.text }} <span class="text-muted">({{ item.date }})</span></li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

<div class="mt-5"></div>

## Award

<ul class="mb-2">
{% for award in site.data.bio.award %}
  <li>
    {{ award.detail }} <span class="text-muted">({{ award.date }})</span>
    {% if award.items.size > 0 %}
    <ul>
    {% for item in award.items %}
      <li>{{ item }}</li>
    {% endfor %}
    </ul>
    {% endif %}
  </li>
{% endfor %}
</ul>
