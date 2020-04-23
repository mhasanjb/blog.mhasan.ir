---
layout: default
permalink: /applications/
title: Application
---

<div class="posts font-small">

    <span>0</span>
    <!-- Categories -->
    {% for applications in applications.categories %}
        {{applications.categories}}
    {% endfor %}
    <!-- Categories -->

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
