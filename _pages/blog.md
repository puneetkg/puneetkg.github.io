---
layout: collection
title: "Blog"
entries_layout: grid
classes: wide
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
