---
title: "Posts"
layout: posts
permalink: /blog/
entries_layout: grid
author_profile: True
classes: wide
---

{% for post in site.posts %}
  {% include archive-single.html type="left" %}
{% endfor %}
