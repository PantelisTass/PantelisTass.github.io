---
layout: archive
title: "Notes"
permalink: /classes/
author_profile: true
---

{% include base_path %}

<h1>Imperial maths undergraduate courses</h1>
{% for post in site.classes reversed %}
  {% if post.type == "Imperial" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

