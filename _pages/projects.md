---
title: "Projects"
permalink: /projects/
layout: single
classes: wide
entries_layout: grid

header: 
    overlay_image: "../assets/img/header/koegl_down.jpeg"
---

{% assign project_pages = site.pages
  | where_exp: "p", "p.url != nil"
  | where_exp: "p", "p.url contains '/projects/'"
  | where_exp: "p", "p.url != '/projects/'"
  | sort: "title" %}

{% for p in project_pages %}
  {% include archive-single.html type="grid" post=p link=p.external_url %}
{% endfor %}
