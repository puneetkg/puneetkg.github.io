---
layout: archive
title: Mindset
entries_layout: grid
permalink: /blog/
collection: portfolio
author_profile: true
header:
 overlay_image: "/images/Articles.jpg"
---

{% for post in site.posts %}
{% if post.category =='blog' %}

  {% include archive-single.html %}
{% endif %}
{% endfor %}
