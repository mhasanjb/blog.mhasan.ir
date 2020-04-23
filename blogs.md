---
layout: default
title: Blog
---

{% for blogs in site.blogs %}

<a href="{{ blogs.url | prepend: site.baseurl }}">
  <h2>{{ blogs.title }}</h2>
</a>

<p class="post-excerpt">{{ blogs.description | truncate: 160 }}</p>

{% endfor %} 
