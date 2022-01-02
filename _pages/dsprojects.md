---
layout: archive
permalink: /projects/
title: "Projects"
author_profile: true
header:
 overlay_image: "/images/header_image.png"
---

{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}
