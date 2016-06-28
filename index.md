---
layout: page
title: psanxiao's web
tagline: Entrepreneur (http://icarto.es ), software developer, maps lover, free software enthusiast, triathlete's trainee... not necessarily in that order
---
{% include JB/setup %}

<ul >
    {% for post in site.posts limit:5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}"><b>{{ post.title }}</b></a></li>
        {{ post.content | strip_html | truncatewords:100}}<br>
            <a href="{{ post.url }}">Read more...</a><br><br>
    {% endfor %}
</ul>


<a href="/archive.html">[All posts]</a>

<h4>Categories</h4>
<ul class="tag_box inline">
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>