---
layout: archive
title: "Classes Taken"
permalink: /classes/
author_profile: true
---

{% include base_path %}


{% for post in site.classes reversed%}
  {% include archive-single.html %}
{% endfor %}
