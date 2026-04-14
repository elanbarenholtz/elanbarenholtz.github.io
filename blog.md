---
layout: page
title: Blog
subtitle: Writing on cognition, AI, and the autoregressive mind
permalink: /blog/
---

<div class="narrow">
  <ul class="post-list">
    {% for post in site.posts %}
    <li class="post-item">
      <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
      {% if post.tags %}
      <div class="post-tags">
        {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </li>
    {% endfor %}
  </ul>

  {% if site.posts.size == 0 %}
  <p style="color: var(--text-light); text-align: center; padding: 3rem 0;">
    Posts coming soon. Follow on <a href="https://substack.com/@generativebrain">Substack</a> for longer-form writing.
  </p>
  {% endif %}
</div>
