---
layout: page_with_back
title: Projects
permalink: /projects/
---

## Projects

Welcome to my projects! Here, you'll find various things I've worked on.

<div class="tags-filter">
  <span class="tag-item {% if page.tag == nil %}active{% endif %}">
    <a href="{{ '/projects/' | relative_url }}" data-tag="all">all</a>
  </span>
  {% assign project_tags = site.projects | map: 'tags' | compact | flatten | uniq | sort %}
  {% for tag in project_tags %}
    <span class="tag-item">
      <a href="#" data-tag="{{ tag }}">#{{ tag }}</a>
    </span>
  {% endfor %}
</div>

<ul class="project-list">
  {% for project in site.projects %}
    <li class="project-item" data-tags="{{ project.tags | join: ' ' }}">
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
      {% if project.description %}
        <span class="subitem">({{ project.description }})</span>
      {% endif %}
      {% if project.tags %}
        <div class="project-tags">
          {% for tag in project.tags %}
            <span class="tag-label">#{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const tagLinks = document.querySelectorAll('.tag-item a');
  const projects = document.querySelectorAll('.project-item');
  
  tagLinks.forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      const selectedTag = this.getAttribute('data-tag');
      
      // Update active state of tag links
      tagLinks.forEach(tl => tl.parentElement.classList.remove('active'));
      this.parentElement.classList.add('active');
      
      // Show/hide projects based on selected tag
      projects.forEach(project => {
        if (selectedTag === 'all') {
          project.style.display = '';
        } else {
          const projectTags = project.getAttribute('data-tags').split(' ');
          project.style.display = projectTags.includes(selectedTag) ? '' : 'none';
        }
      });
    });
  });
});
</script>
