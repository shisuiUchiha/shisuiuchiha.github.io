---
layout: default
title: Home
---

# My Thoughts

My views, essays and explanations about technology, science, world affairs, travel and more.

---

## Topics

- [Technology](/topics/technology)
- [Science](/topics/science)
- [Global Affairs](/topics/global-affairs)
- [Economy](/topics/economy)
- [Travel](/topics/travel)
- [General](/topics/general)

---

## Latest Posts

{% for post in site.posts limit:6 %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}