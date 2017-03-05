---
layout: page
title: Dojo News
permalink: /news/
---

{% for post in site.posts limit:10 %}
<article class="home">
    <h2>
        <a href="{{ site.BASE_PATH }}{{ post.url }}">{{post.title}}</a>
    </h2>
    
    <p> {% if post.author %}
            <strong>Author:</strong>{{post.author}} •
        {% endif %} 
        <strong>Published:</strong>{{ post.date | date: "%b %-d, %Y" }}
    </p>
</article>
{% endfor %}