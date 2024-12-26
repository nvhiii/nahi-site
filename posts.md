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

<div class="terminal-blog-container">
  {% for post in site.posts %}
    <a href="{{ site.baseurl }}{{ post.url }}" class="terminal-post-link">
      <div class="terminal-post-card" data-tags="{{ post.tags | join: ' ' }}">
        <div class="terminal-window-header">
          <div class="terminal-window-dots">
            <span class="terminal-dot terminal-dot-red"></span>
            <span class="terminal-dot terminal-dot-yellow"></span>
            <span class="terminal-dot terminal-dot-green"></span>
          </div>
          <div class="terminal-window-title">{{ post.title }}</div>
        </div>
        <div class="terminal-window-content">
          <div class="terminal-post-title">{{ post.title }}</div>
          <div class="terminal-post-meta">{{ post.date | date: "%B %d, %Y" }}</div>
          {% if post.tags %}
            <div class="terminal-post-tags">
              {% for tag in post.tags %}
                <span class="terminal-tag">#{{ tag }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </div>
      </div>
    </a>
  {% endfor %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const tagLinks = document.querySelectorAll('.tag-item a');
  const posts = document.querySelectorAll('.terminal-post-card');
  
  tagLinks.forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      const selectedTag = this.getAttribute('data-tag');
      
      tagLinks.forEach(tl => tl.parentElement.classList.remove('active'));
      this.parentElement.classList.add('active');
      
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
