---
layout: default
permalink: /applications/
title: Application
---

<div class="applications font-small">
    {% for applications in site.applications %}
    <article class="applications">

        <h4>
            <span class="post-date font-small"> {{ applications.date | date: "%B %e, %Y" }} » </span>
            <a href="{{ site.baseurl }}{{ applications.url }}">{{ applications.title }}</a>
        </h4>

        <!--<div class="entry">
            <span>{{ applications.excerpt }}</span>
        </div>

        <a href="{{ site.baseurl }}{{ applications.url }}" class="read-more">Read More</a>-->
    </article>
    {% endfor %}
</div>
