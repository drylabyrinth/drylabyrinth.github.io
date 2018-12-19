---
title: People
layout: default
permalink: /people/
---
{% assign sorted_people = site.people | sort: 'last_name' %}

<div class="grid__wrapper">
{% for person in sorted_people %}
  {% include people.html type = "grid" %}
{% endfor %}
</div>
