---
layout: default
title: Home
---

# CAT Preparation Blog

Welcome to the CAT preparation resource hub.

## Latest Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}