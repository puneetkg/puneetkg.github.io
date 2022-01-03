---
layout: archive
title: "Articles"
permalink: /articles/
author_profile: true
header:
 overlay_image: "/images/Articles.jpg"
---

{% for post in site.posts %}
{% if post.category =='blog' %}

  {% include archive-single.html %}
{% endif %}
{% endfor %}
