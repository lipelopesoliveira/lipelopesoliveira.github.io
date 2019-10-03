---
title: "Posts"
layout: collection
permalink: /blog/
author_profile: True
entries_layout: grid
classes: wide
---

{% for post in site.posts limit: 4 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="intro" type="center" %}
{% include feature_row %}
{% include feature_row id="feature_row2" type="left" %}
{% include feature_row id="feature_row3" type="right" %}
{% include feature_row id="feature_row4" type="center" %}
