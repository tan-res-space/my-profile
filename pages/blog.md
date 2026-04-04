---
layout: page
title: Blog
subtitle: Thoughts on AI, machine learning, and building practical solutions.
permalink: /pages/blog/
---

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <div class="post-list-meta">{{ post.date | date: "%B %-d, %Y" }}</div>
    <a href="{{ post.url | relative_url }}" class="post-list-title">{{ post.title }}</a>
    {% if post.excerpt %}
    <p class="post-list-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>Coming soon. Stay tuned for posts on AI/ML research, practical data science, and lessons from building production systems.</p>
{% endif %}
