---
layout: default
title: Application
---

<div class="blogs">
  {% for blogs in site.blogs %}
    <article class="blogs">

      <h1><a href="{{ site.baseurl }}{{ blogs.url }}">{{ blogs.title }}</a></h1>

      <div class="entry">
        {{ blogs.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ blogs.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>

