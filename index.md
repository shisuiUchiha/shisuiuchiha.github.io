---
layout: default
title: Home
---

# My Thoughts

my views, essays and explanations about technology, coding, world affairs and travel.

---

## Topics

- [Technology](/topics/technology)
- [Coding](/topics/coding)
- [Global Affairs](/topics/global-affairs)
- [Economy](/topics/economy)
- [Travel](/topics/travel)

---

## Latest Posts

{% for post in site.posts limit:6 %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}