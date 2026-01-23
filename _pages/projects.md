---
title: "Projects"
permalink: /projects/
layout: single
classes: wide
entries_layout: grid
author_profile: false

header: 
    overlay_image: "../assets/img/header/koegl_down.jpeg"
---

{% assign project_pages = site.html_pages
  | where_exp: "p", "p.path contains '_pages/projects/'"
  | sort: "title" %}

{% for p in project_pages %}
  {% include archive-single.html type="grid" post=p %}
{% endfor %}

