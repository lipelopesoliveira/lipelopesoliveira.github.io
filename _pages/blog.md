---
title: "Posts"
layout: collection
permalink: /blog/
author_profile: True
entries_layout: grid
classes: wide
---
{% include feature_row id="intro" type="grid" %}
{% for post in site.posts limit: 25 %}
  {% include archive-single.html type="center" %}
{% endfor %}
{% include feature_row id="intro" type="center" %}
