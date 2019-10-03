---
title: "Posts"
layout: collection
permalink: /blog/
entries_layout: grid
classes: wide
---
{% include feature_row id="intro" type="left" %}
{% for post in site.posts %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="intro" type="center" %}
