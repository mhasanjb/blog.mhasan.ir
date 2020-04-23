---
layout: default
title: Application
---

<div class="posts font-small">
    <span>Changed</span>
    {% for applications in site.categories %}
        <h1>{{ applications.categories }}</h1>
    {% endfor %}

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
