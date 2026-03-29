---
layout: default
title: Home
---

<div class="hero">
  <h1>Welcome to My Blog</h1>
  <p>Thoughtful explorations across technology, science, global affairs, economy, and travel</p>
  <div class="hero-buttons">
    <a href="#latest-posts" class="btn btn-primary">Read Latest Posts</a>
    <a href="/about" class="btn btn-secondary">About Me</a>
  </div>
</div>

<div class="container">
  <div class="section-title">
    <h2>Browse by Topic</h2>
    <p>Explore articles organized by category</p>
  </div>

  <div class="topics-grid">
    <a href="/topics/technology" class="topic-card technology">
      <div class="topic-icon">💻</div>
      <h3>Technology</h3>
      <p>Tech insights & coding</p>
    </a>
    
    <a href="/topics/science" class="topic-card science">
      <div class="topic-icon">🔬</div>
      <h3>Science</h3>
      <p>Scientific discoveries</p>
    </a>
    
    <a href="/topics/global-affairs" class="topic-card global-affairs">
      <div class="topic-icon">🌍</div>
      <h3>Global Affairs</h3>
      <p>World events & politics</p>
    </a>
    
    <a href="/topics/economy" class="topic-card economy">
      <div class="topic-icon">💰</div>
      <h3>Economy</h3>
      <p>Finance & economics</p>
    </a>
    
    <a href="/topics/travel" class="topic-card travel">
      <div class="topic-icon">✈️</div>
      <h3>Travel</h3>
      <p>Adventures & experiences</p>
    </a>
    
    <a href="/topics/general" class="topic-card general">
      <div class="topic-icon">📝</div>
      <h3>General</h3>
      <p>Miscellaneous thoughts</p>
    </a>
  </div>

  <div id="latest-posts" class="section-title">
    <h2>Latest Posts</h2>
    <p>Fresh perspectives on diverse topics</p>
  </div>

  <div class="posts-grid">
    {% for post in site.posts limit:6 %}
    <div class="post-card">
      <div class="post-meta">
        <span class="post-category {{ post.categories[0] }}">{{ post.categories[0] | capitalize }}</span>
        <span class="post-meta-item">📅 {{ post.date | date: "%B %d, %Y" }}</span>
      </div>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="post-card-excerpt">
        {% if post.excerpt %}
          {{ post.excerpt | strip_html | truncatewords: 25 }}
        {% else %}
          {{ post.content | strip_html | truncatewords: 25 }}
        {% endif %}
      </div>
      <div class="post-card-footer">
        <a href="{{ post.url }}" class="read-more">Read More</a>
      </div>
    </div>
    {% endfor %}
  </div>
</div>
