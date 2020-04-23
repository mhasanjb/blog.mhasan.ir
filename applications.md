---
layout: default
title: Application
---

{% for applications in site.applications %}

<a href="{{ applications.url | prepend: site.baseurl }}">
  <h2>{{ applications.title }}</h2>
</a>

<p class="post-excerpt">{{ applications.description | truncate: 160 }}</p>

{% endfor %} 
