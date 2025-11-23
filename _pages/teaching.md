---
layout: teaching_fullwidth
title: "Teaching"
permalink: /teaching/
body_class: teaching-page
---

{% include base_path %}

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

