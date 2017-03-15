---
layout: page
title: _#voyaserunironman
header: _#voyaserunironman
group: navigation
---
{% include JB/setup %}

Esta sección es un recopilatorio de los posts etiquetados bajo la categoría **#voyaserunironman**, en los cuales cuento mi experiencia de preparación para intentar hacer mi primer triatlón distancia Ironman (3,8 km swin - 180 km bike - 42 Km run).

***

<ul >
    {% for post in site.categories.voyaserunironman %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}"><b>{{ post.title }}</b></a></li>
        {{ post.content | strip_html | truncatewords:100}}<br>
            <a href="{{ post.url }}">Read more...</a><br><br>
    {% endfor %}
</ul>