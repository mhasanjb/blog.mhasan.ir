---
layout: default
title: Application
---

{% for application in site.applications %}

<a href="{{ application.url | prepend: site.baseurl }}">
  <h2>{{ application.title }}</h2>
</a>

<p class="post-excerpt">{{ application.description | truncate: 160 }}</p>

{% endfor %} 
