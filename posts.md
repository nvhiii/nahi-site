---
layout: page_with_back
title: Blog
---

## Blog

Welcome to my blog! Here, you'll find posts about things I find interesting or worth sharing.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span class="subitem">({{ post.date | date: "%b %d, %Y" }})</span>
    </li>
  {% endfor %}
</ul>
