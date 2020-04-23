---
layout: default
title: Blog
---

{% for blog in site.blogs %}

<a href="{{ blog.url | prepend: site.baseurl }}">
  <h2>{{ blog.title }}</h2>
</a>

<p class="post-excerpt">{{ blog.description | truncate: 160 }}</p>

{% endfor %} 
