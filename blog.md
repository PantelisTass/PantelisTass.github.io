---
layout: default
title: Blog
permalink: /blog/
---

<div class="content-card">
  <h2>Welcome to my blog page!</h2>

   Here you will find some of my thoughts on topics in maths and beyond that interest me at any given time.

   <h1>Blog Posts</h1>
  
  {% for post in site.posts %}
    <article style="margin-bottom: 3rem;">
      <header>
      <span style="color: #888; font-size: 0.9rem;">{{ post.date | date: "%B, %Y" }}</span>
        <h2 style="margin-top: 5px;">
          {% if post.permalink %}
            {{ post.title }}
          {% else %}
            <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #222;">{{ post.title }}</a>
          {% endif %}
        </h2>
      </header>

      <div class="post-excerpt" style="margin: 1rem 0; line-height: 1.6;">
        {% if post.excerpt %}
          {{ post.excerpt | strip_html | truncatewords: 100 }}
        {% endif %}
      </div>

      <footer style="font-weight: bold;">
        <a href="{{ post.permalink | default: post.url | relative_url }}">Read more &rarr;</a>
      </footer>
    </article>
  {% endfor %}
</div>