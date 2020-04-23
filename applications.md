---
layout: default
title: Application
---

<div class="posts">
  {% for applications in site.applications %}
    <article class="applications">

      <h1><a href="{{ site.baseurl }}{{ applications.url }}">{{ applications.title }}</a></h1>

      <div class="entry">
        {{ applications.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ applications.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
