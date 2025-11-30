---
layout: classes_fullwidth
title: "Course Notes & Classes"
permalink: /classes/
body_class: classes-page
descriotion: A collection of some of my notes, coursework, or projects I have written up.
---

{% include base_path %}

{% assign sorted_classes = site.classes | sort: "year" | reverse %}

{% for post in sorted_classes %}
  {% include archive-single.html %}
{% endfor %}

