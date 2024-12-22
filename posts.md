---
layout: page_with_back
title: Blog
permalink: /posts/
---

## Blog

Welcome to my blog! Here, you'll find posts about things I find interesting or worth sharing.

<div class="tags-filter">
  <span class="tag-item {% if page.tag == nil %}active{% endif %}">
    <a href="{{ '/posts/' | relative_url }}" data-tag="all">all</a>
  </span>
  {% assign tags = site.posts | map: 'tags' | compact | flatten | uniq | sort %}
  {% for tag in tags %}
    <span class="tag-item">
      <a href="#" data-tag="{{ tag }}">#{{ tag }}</a>
    </span>
  {% endfor %}
</div>

<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item" data-tags="{{ post.tags | join: ' ' }}">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <span class="subitem">({{ post.date | date: "%b %d, %Y" }})</span>
      {% if post.tags %}
        <div class="post-tags">
          {% for tag in post.tags %}
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
  const posts = document.querySelectorAll('.post-item');
  
  tagLinks.forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      const selectedTag = this.getAttribute('data-tag');
      
      // Update active state of tag links
      tagLinks.forEach(tl => tl.parentElement.classList.remove('active'));
      this.parentElement.classList.add('active');
      
      // Show/hide posts based on selected tag
      posts.forEach(post => {
        if (selectedTag === 'all') {
          post.style.display = '';
        } else {
          const postTags = post.getAttribute('data-tags').split(' ');
          post.style.display = postTags.includes(selectedTag) ? '' : 'none';
        }
      });
    });
  });
});
</script>
