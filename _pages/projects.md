---
title: "Projects"
permalink: /projects/
layout: single
author_profile: true
classes: wide
header: 
    overlay_image: "../assets/img/header/Ginpeak.jpg"
entries_layout: grid
---

{% assign items = site.projects | sort: "title" %}

{% for post in items %}
  {% include archive-single.html type="grid" %}
{% endfor %}
