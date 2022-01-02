---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
header:
 overlay_image: "/images/header_image.png"
---

{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
