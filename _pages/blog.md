---
layout: splash
permalink: /blog/
title: "Posts about nanoscience and computation"
author_profile: True
header:
  image: "/images/header.jpg"
---

{% for post in site.posts limit: 5 %}
  {% include archive-single.html %}
{% endfor %}

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
