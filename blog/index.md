---
title: Blog
description: Read our latest insights and ideas.
---

<section class="hero">
  <h1>Insights &amp; Ideas</h1>
</section>

<section class="section">
  <div class="container">
    {% if site.posts == empty %}
      <p>No posts found. Check back soon!</p>
    {% else %}
      {% for post in site.posts %}
        <article class="post-preview">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
          <small>{{ post.date | date: "%B %-d, %Y" }}</small>
        </article>
      {% endfor %}
    {% endif %}
  </div>
</section>
