---
layout: page_with_back
title: Projects
permalink: /projects/
---

## Projects

Here are some of the projects I'm proud of:

<ul>
  {% for project in site.projects %}
    <li><a href="{{ project.url | relative_url }}">{{ project.title }}</a></li>
  {% endfor %}
</ul>
