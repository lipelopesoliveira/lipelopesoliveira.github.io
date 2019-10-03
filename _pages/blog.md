---
title: "Posts"
layout: collection
permalink: /blog/
author_profile: True
entries_layout: grid
classes: wide
---

{% include feature_row id="intro" type="center" %}
{% for post in site.posts limit: 5 %}
  {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}
