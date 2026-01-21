---
title: "Projects"
permalink: /projects/
layout: single
classes: wide
entries_layout: grid
author_profile: true
---

{% assign project_pages = site.pages
  | where_exp: "p", "p.url != nil"
  | where_exp: "p", "p.url contains '/projects/'"
  | where_exp: "p", "p.url != '/projects/'"
  | sort: "title" %}

{% for post in project_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
