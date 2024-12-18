---
layout: home
title: Home
---

<div class="header-container">
  <header>
    <h1>nahi@Nahi</h1>
  </header>
</div>

## Directory

- [About]({{ site.baseurl }}/about/)
- [Projects]({{ site.baseurl }}/projects/)
  <ul>
  {% for project in site.projects %}
    <li class="subitem"><a href="{{ project.url }}">{{ project.title }}</a></li>
  {% endfor %}
  </ul>
- [Blog]({{ site.baseurl }}/posts/)
  <ul>
  {% for post in site.posts %}
    <li class="subitem">{{ post.date | date: "%b %d, %Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
