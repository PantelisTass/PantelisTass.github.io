---
layout: teaching_fullwidth
title: "Teaching"
permalink: /teaching/
body_class: teaching-page
description: A collection of all teaching responsibilities I have had.
---

{% include base_path %}

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

