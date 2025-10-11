---
layout: page
title: "Blog"
permalink: /blog/
---

<center><img src="/images/blog.jpg" width="1200"  align="center"></center>

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
