---
title: People
layout: default
permalink: /people/
people:
  - title: "People"
    excerpt: "OHSU Computation consists of many groups, staff, faculty, and students."
---
{% assign sorted_people = site.people | sort: 'last_name' %}
{% include feature_row id= "people" type = "center" %}

<div class="grid__wrapper">
{% for person in sorted_people %}
  {% include people.html type = "grid" %}
{% endfor %}
</div>
