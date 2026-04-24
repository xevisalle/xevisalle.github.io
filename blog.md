---
layout: default
title: Blog
---

## Blog

<div class="post-list">
{% if site.posts.size > 0 %}
  {% for post in site.posts %}
  <a class="post-card" href="{{ post.url | relative_url }}">
    <div class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</div>
    <div class="post-card-title">{{ post.title }}</div>
    {% if post.excerpt %}
    <div class="post-card-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</div>
    {% endif %}
  </a>
  {% endfor %}
{% else %}
  <div class="no-posts">// no posts yet — check back soon</div>
{% endif %}
</div>
