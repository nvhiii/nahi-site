---
layout: default
title: Home
---

<div class="back-to-home-placeholder"></div>
<header>
  <h1>nahi@Nahi</h1>
</header>

## Directory

- [About]({{ site.baseurl }}/about/)
- [Socials / Resume]({{ site.baseurl }}/contact/)
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
