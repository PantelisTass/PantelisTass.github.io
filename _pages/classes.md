---
layout: archive
title: "Notes"
permalink: /classes/
author_profile: true
---

{% include base_path %}

[Analysis of PDEs](/files/Analysis of PDE.pdf)

<h1>Part III Cambridge maths courses</h1>
{% for post in site.classes reversed %}
  {% if post.type == "Part III" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


<h1>Imperial maths undergraduate courses</h1>
{% for post in site.classes reversed %}
  {% if post.type == "Imperial" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

