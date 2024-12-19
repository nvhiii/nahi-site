---
layout: post
title: "Migrating to Jekyll"
date: 2024-12-19 00:55:50 +0000
categories: hosting jekyll ssgs
footnotes:
  - Reddit
  - Hacked Jekyll Theme
  - No Style Please Jekyll Theme
---

### Preface / TLDR;

Honestly, I was bored of my old site. I thought it was too "vibrant," aka it didn't match my aesthetic. I also didn't want to create everything in pure HTML and CSS since it takes a precious resource I don't have much of — time. So, as any smart fella does, I looked at some portfolios of friends and people I look up to. I'll admit that this was entertaining, but you know that primal urge of being unique? Yeah. I didn't want to simply spam Bootstrap / Tailwind / React + Netlify as a personal site.

Theoretically, I wanted a site that wasn't bloated with JS and one that provided a pleasant viewing experience on any UI. I'll admit this place is a continuous W.I.P., so don't expect it to be perfect, you snobs, lol.

Anyways, back to the content of my site. Since I wanted this site to collectively demonstrate the inner workings of my brain, I thought it would be best to include:

- A blog (which I'll hopefully add commenting to in the future),
- A place to add cool things I tinker and dabble in,
- And some socials.

I think this would show my thoughts, thinking process, and how I want to be perceived.

### Why Static Site Generators (SSGs)?

The best solution I found was static site generators (SSGs)<sup><a href="#footnote-1">1</a></sup>. At first, I was overjoyed! "Aha!"... but we all know that nothing is ever _that_ straightforward. I found myself tinkering with the Hugo SSG and learning TOML at the same time, and at first, everything was going smoothly.

However, when I wanted to implement a specific theme and customize it to my needs, I encountered a problem where I was not able to override the default header theme, which made me mald. (I'm not bashing Hugo; it's probably because of my one-day experience using TOML, tbh).

### Switching to Jekyll

After reconvening the next day, I decided to create my site using another SSG: Jekyll. I found onboarding, creating sites, and deploying them locally via Jekyll very straightforward as well, but the sheer amount of documentation and community themes just made it that much more appealing.

Some particular Jekyll themes I kept referring to while creating this portfolio are the [Hacked Jekyll Theme](#footnote-2)<sup><a href="#footnote-2">2</a></sup> and the [No-Style-Please Theme](#footnote-3)<sup><a href="#footnote-3">3</a></sup>. I actually use No-Style-Please as my theme, but I customize it to cater to my preferences.
