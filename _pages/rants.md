---
layout: archive
permalink: /rants/
title: "Random Rants and Observations"
author_profile: true
header:
 overlay_image: "/images/learning.jpg"
---

{% for post in site.rants %}
  {% include archive-single.html %}
{% endfor %}
