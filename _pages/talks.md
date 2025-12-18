---
layout: talks_fullwidth
title: "Talks"
permalink: /talks/
body_class: talks-page
description: A list of talks I have given at conferences and beyond
---
<p>talkmap_link = {{ site.talkmap_link }}</p>
<p>number of talks = {{ site.talks | size }}</p>

{% if site.talkmap_link == true %}

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}