---
title: "Posts"
layout: posts
permalink: /blog/
entries_layout: grid
author_profile: False
classes: wide
---

{% for post in site.posts %}
  {% include archive-single.html type="grid" %}
{% endfor %}
