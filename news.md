---
layout: page
title: Dojo News
permalink: /news/
---

{% for post in paginator.posts %}
<article class="home">
    <span class="post-date">{{ post.date }}</span>
    <h2><a href="{{ site.BASE_PATH }}{{ post.url }}">{{post.title}}</a></h2>
    
</article>
{% endfor %}