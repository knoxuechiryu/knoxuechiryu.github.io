---
layout: page
title: Dojo News
permalink: /news/
---


<div class="col-sm-8 col-sm-offset-2">
{% for post in site.posts limit:10 %}
<div class="row postrow">
<article class="news">
    <h2 >
        <a href="{{ site.BASE_PATH }}{{ post.url }}">{{post.title}}</a>
    </h2>
    <p class="meta"> {% if post.author %}
            <strong>Author:</strong>{{post.author}} •
        {% endif %} 
        <strong>Published:</strong>{{ post.date | date: "%b %-d, %Y" }}
    </p>
    {% if post.image %}
    <div class="image-wrapper">
        <img src="{{ site.BASE_PATH }}{{ post.image }}" alt="{{post.imageMeta}}" />        
    </div>
    <p class="clear-fix"></p>
    {% endif %}
    {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
        <p class="pull-right"><a href="{{ site.BASE_PATH }}{{ post.url }}"><strong>Continue Reading</strong></a></p>
        <p class="clearfix"></p>
    {% endif %}
</article>
</div>
{% endfor %}
</div>