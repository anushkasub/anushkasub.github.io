---
layout: default
title: Blog
permalink: /blog/
---

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%b %-d, %Y" }}</time>
    <div>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.description %}<p class="post-excerpt">{{ post.description }}</p>{% else %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty-note">No posts yet. Check back soon.</p>
{% endif %}
