---
layout: home
title: Home
---

Welcome to my site!

## Recent Posts

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endfor %} 