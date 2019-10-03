---
title: "Posts"
layout: collection
permalink: /blog/
entries_layout: grid
---
{% for post in site.posts %}
  {% include archive-single.html type="grid" %}
{% endfor %}
