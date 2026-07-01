---
layout: default
title: "Home"
---

<section class="hero">
  <p class="eyebrow">Welcome</p>
  <h1>A calmer, more polished home for notes and writing.</h1>
  <p class="hero-copy">
    This site now focuses on readable long-form posts, a cleaner archive, and a more intentional presentation inspired by modern digital gardens.
  </p>
  <div class="hero-actions">
    <a class="button button-primary" href="#latest">Read the latest post</a>
    <a class="button" href="https://www.linkedin.com/in/pramodkr/" target="_blank" rel="noreferrer">Connect on LinkedIn</a>
  </div>
</section>

<section id="latest" class="content-panel">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Latest writing</p>
      <h2>Recent posts</h2>
    </div>
    <p>Short, practical notes and references worth revisiting.</p>
  </div>

  {% if site.posts.size > 0 %}
    <div class="post-feed">
      {% for post in site.posts %}
        <article class="post-card">
          <p class="post-card-meta">{{ post.date | date: "%B %d, %Y" }}</p>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | strip_html | normalize_whitespace | truncate: 180 }}</p>
        </article>
      {% endfor %}
    </div>
  {% else %}
    <div class="empty-state">
      <p>No posts yet.</p>
    </div>
  {% endif %}
</section>

<section id="archive" class="content-panel">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Archive</p>
      <h2>Browse everything in one place</h2>
    </div>
    <p>Each note stays easy to scan, date, and revisit.</p>
  </div>

  {% if site.posts.size > 0 %}
    <div class="archive-list">
      {% for post in site.posts %}
        <div class="archive-item">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %d, %Y" }}</time>
        </div>
      {% endfor %}
    </div>
  {% else %}
    <div class="empty-state">
      <p>The archive will appear here as new posts are published.</p>
    </div>
  {% endif %}
</section>
