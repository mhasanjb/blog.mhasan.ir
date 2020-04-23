---
layout: default
permalink: /applications/
title: Application
---

<div class="posts font-small">

    <span>Change001</span>
    <!-- Categories -->
    <div id="archives">
        {% for categories in applications.categories %}
        <div class="archive-group">
            {% capture category_name %}{{ category | first }}{% endcapture %}
            <div id="#{{ category_name | slugize }}"></div>
            <p></p>

            <h3 class="category-head">{{ category_name }}</h3>
            <a name="{{ category_name | slugize }}"></a>
        </div>
        {% endfor %}
    </div>
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
