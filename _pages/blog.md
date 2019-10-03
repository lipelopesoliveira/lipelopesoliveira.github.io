---
title: "Posts"
layout: collection
permalink: /blog/
author_profile: True
entries_layout: grid
classes: wide
---

{% include feature_row id="intro" type="grid" %}
{% for post in post_pagination %}
  {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}
