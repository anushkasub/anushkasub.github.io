---
layout: default
title: Quotes
permalink: /quotes/
published: false
---

A few lines I keep coming back to.

<div class="quotes">
{% for q in site.data.quotes %}
<figure class="quote">
  <blockquote>{{ q.text | markdownify }}</blockquote>
  <figcaption>&mdash; {{ q.author }}{% if q.source %}, <cite>{{ q.source }}</cite>{% endif %}</figcaption>
</figure>
{% endfor %}
</div>
