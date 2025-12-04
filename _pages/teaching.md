---
layout: teaching_fullwidth
title: "Teaching"
permalink: /teaching/
body_class: teaching-page
description: A collection of all teaching responsibilities I have had.
---
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

{% include base_path %}

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

