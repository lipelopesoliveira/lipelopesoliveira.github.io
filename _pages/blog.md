---
title: "Posts"
layout: collection
permalink: /blog/
author_profile: True
entries_layout: grid
classes: wide
---

{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="intro" type="center" %}
{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row %}
{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="feature_row2" type="left" %}
{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="feature_row3" type="right" %}
{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
{% include feature_row id="feature_row4" type="center" %}
{% for post in site.posts limit: 3 %}
  {% include archive-single.html type="grid" %}
{% endfor %}
