---
layout: default
title: Application
---

<h1>{{ applications.categories }}</h1>
<div class="posts font-small">
  {% for applications in site.applications %}
    <article class="applications">
      
      <h4><a href="{{ site.baseurl }}{{ applications.url }}">{{ applications.title }}</a></h4>

      <div class="entry">
        <span>{{ applications.excerpt }}</span>
      </div>

      <a href="{{ site.baseurl }}{{ applications.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
