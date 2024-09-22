---
layout: archive
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- Publications Section -->
<h1>Publications</h1>
{% for post in site.publications reversed %}
  {% if post.type == 'publications' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<!-- Preprints Section -->
<h1>Preprints</h1>
{% for post in site.publications reversed %}
  {% if post.type == 'preprints' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
