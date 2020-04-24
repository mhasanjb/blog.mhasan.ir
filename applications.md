---
layout: default
permalink: /applications/
title: Application
---

<div class="applications font-small">
    <!-- Category -->
    <span>0</span>
    {% for applications in site.applications %}
        {{applications.categories}}
    {% endfor %}
    <!-- Category -->

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
