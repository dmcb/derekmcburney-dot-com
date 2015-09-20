---
layout: default
title: Blog
permalink: /blog/
---

<div class="home">
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <span class="post-meta">
          {{ post.date | date: "%b %-d, %Y" }}<!-- {% if post.tags %}, {% endif %}
          {% for tag in post.tags %}
          <a class="tag">{{ tag }}</a>
          {% endfor %} -->
        </span>
        <p>{{ post.description }}</p>
      </li>
    {% endfor %}
  </ul>
</div>