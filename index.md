---
layout: default
title: Nahi Khan
---

<div class="header-container">
  <header>
    <h1>nahi@Nahi</h1>
  </header>
</div>

## Directory

- <a href="{{ site.baseurl }}/about/" class="styled-link">[About]</a>
- <a href="{{ site.baseurl }}/projects/" class="styled-link">[Projects]</a>
  <ul>
  {% for project in site.projects %}
    <li class="subitem"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
  {% endfor %}
  </ul>
- <a href="{{ site.baseurl }}/posts/" class="styled-link">[Blog]</a>
  <ul>
  {% for post in site.posts %}
    <li class="subitem"><span class="date">{{ post.date | date: "%b %d, %Y" }}</span> - <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
- <a href="{{ site.baseurl }}/sitemap.xml" class="styled-link">[SiteMap]</a>
