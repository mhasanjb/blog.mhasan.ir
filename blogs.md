---
layout: default
permalink: /blogs/
title: Blogs
---

<div class="blogs font-small">
  {% for blogs in site.blogs %}
    <article class="blogs">

      <h4><a href="{{ site.baseurl }}{{ blogs.url }}">{{ blogs.title }}</a></h4>

      <div class="entry">
        <span>{{ blogs.excerpt }}</span>
      </div>

      <a href="{{ site.baseurl }}{{ blogs.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>

