---
layout: archive
title: "Data Analysis"
permalink: /projects/
author_profile: true
header:
 overlay_image: "/images/project.jpg"
---

{% for post in site.posts %}
{% if post.category =='project' %}

  {% include archive-single.html %}
{% endif %}
{% endfor %}
