---
layout: archive
title: ""
permalink: /extra/
author_profile: true
---

<div class="post-list">
  {% for post in site.posts %}
    <div class="post-card">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
      {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
      {% endif %}
    </div>
  {% endfor %}
</div>

<style>
.post-list {
  display: flex;
  flex-direction: column;
  gap: 1.5em;
  margin: 2em 0;
}
.post-card {
  padding: 1em 1.5em;
  border-radius: 8px;
  background: #f8f9fa;
  box-shadow: 0 2px 6px rgba(0,0,0,0.04);
}
.post-card h3 {
  margin: 0 0 0.3em 0;
}
.post-meta {
  color: #888;
  font-size: 0.95em;
  margin-bottom: 0.5em;
}
.post-excerpt {
  margin: 0;
  color: #444;
}
</style>
