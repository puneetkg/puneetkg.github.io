---
layout: archive
permalink: /articles/
title: "Articles"
author_profile: true
header:
 overlay_image: "/images/learning.jpg"
---

{% for post in site.rants %}
  {% include archive-single.html %}
{% endfor %}
