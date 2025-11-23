---
layout: publications_clean
title: Publications
permalink: /publications/
---

{% if site.author.googlescholar %}
<div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<div class="publications-container">

  <!-- Publications Section -->
  <h1>Publications</h1>
  {% for post in site.publications reversed %}
    {% if post.type == 'publications' %}
      <div class="publication-card">
        <div class="pub-meta">
          <span class="pub-year">{{ post.year }}</span>
          {% if post.venue %}
            • <span class="pub-venue">{{ post.venue }}</span>
          {% endif %}
        </div>

        <h2 class="pub-title">
          {% if post.link %}
            <a href="{{ post.link }}">{{ post.title }}</a>
          {% else %}
            {{ post.title }}
          {% endif %}
        </h2>

        {% if post.authors %}
          <p class="pub-authors">{{ post.authors }}</p>
        {% endif %}

        {% if post.excerpt %}
          <p>{{ post.excerpt }}</p>
        {% endif %}

        <div class="pub-links">
          {% if post.pdf %}<a href="{{ post.pdf | relative_url }}">PDF</a>{% endif %}
          {% if post.code %}<a href="{{ post.code }}">Code</a>{% endif %}
          {% if post.doi %}<a href="https://doi.org/{{ post.doi }}">DOI</a>{% endif %}
        </div>
      </div>
    {% endif %}
  {% endfor %}

  <!-- Preprints Section -->
  <h1>Preprints</h1>
  {% for post in site.publications reversed %}
    {% if post.type == 'preprints' %}
      <div class="publication-card">
        <div class="pub-meta">
          <span class="pub-year">{{ post.year }}</span>
          {% if post.venue %}
            • <span class="pub-venue">{{ post.venue }}</span>
          {% endif %}
        </div>

        <h2 class="pub-title">
          {% if post.link %}
            <a href="{{ post.link }}">{{ post.title }}</a>
          {% else %}
            {{ post.title }}
          {% endif %}
        </h2>

        {% if post.authors %}
          <p class="pub-authors">{{ post.authors }}</p>
        {% endif %}

        {% if post.excerpt %}
          <p>{{ post.excerpt }}</p>
        {% endif %}

        <div class="pub-links">
          {% if post.pdf %}<a href="{{ post.pdf | relative_url }}">PDF</a>{% endif %}
          {% if post.code %}<a href="{{ post.code }}">Code</a>{% endif %}
          {% if post.doi %}<a href="https://doi.org/{{ post.doi }}">DOI</a>{% endif %}
        </div>
      </div>
    {% endif %}
  {% endfor %}

</div>




