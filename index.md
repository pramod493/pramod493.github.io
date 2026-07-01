---
layout: default
title: "Pramod's corner of the web"
page_class: home
---

<section class="hero">
  <div class="hero__content">
    <p class="eyebrow">Personal site</p>
    <h1>A cleaner, more professional home for writing and ideas.</h1>
    <p class="hero__lede">
      I use this space to collect useful notes, share practical technical write-ups, and keep a durable archive of my work on the web.
    </p>
    <div class="hero__actions">
      <a class="button button--primary" href="#latest-posts">Read the blog</a>
      <a class="button button--secondary" href="{{ site.linkedin_url }}">Connect on LinkedIn</a>
    </div>
  </div>
  <aside class="hero__panel">
    <h2>What you'll find here</h2>
    <ul class="feature-list">
      <li>Concise technical articles and references</li>
      <li>Archived writing worth keeping accessible</li>
      <li>A simple index of posts without distractions</li>
    </ul>
  </aside>
</section>

<section class="section-grid">
  <article class="info-card">
    <p class="eyebrow">About</p>
    <h2>Focused, readable content</h2>
    <p>This site is intentionally lightweight, with clear navigation and a format that keeps the writing front and center.</p>
  </article>
  <article class="info-card">
    <p class="eyebrow">Archive</p>
    <h2>Earlier posts are still available</h2>
    <p>If you're looking for older material, the archived blog remains online for reference.</p>
    <a class="text-link" href="{{ site.legacy_blog_url }}">Visit the archived blog</a>
  </article>
</section>

<section class="posts-section" id="latest-posts">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Latest writing</p>
      <h2>Posts</h2>
    </div>
  </div>

  {% if site.posts.size > 0 %}
  <div class="post-list">
    {% for post in site.posts %}
    <article class="post-card">
      <p class="post-card__date">{{ post.date | date: "%B %d, %Y" }}</p>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 24 }}</p>
      <a class="text-link" href="{{ post.url | relative_url }}">Read article</a>
    </article>
    {% endfor %}
  </div>
  {% else %}
  <article class="post-card post-card--empty">
    <h3>No posts yet</h3>
    <p>New writing will appear here as it is published.</p>
  </article>
  {% endif %}
</section>
