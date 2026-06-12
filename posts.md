---
layout: page
title: Posts
permalink: /posts/
---

Hello! 

Here you will find all the latest codes, articles and other things.

---

### All Tracked Entries

<ul class="post-content" style="list-style-type: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5rem;">
      <span class="text-muted" style="font-size: 0.9rem; margin-right: 1rem;">
        {{ post.date | date: "%Y-%m-%d" }}
      </span>
      <strong style="font-size: 1.1rem;">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </strong>
      {% if post.description %}
        <p class="text-muted" style="margin: 0.2rem 0 0 5.5rem; font-size: 0.95rem;">
          {{ post.description }}
        </p>
      {% endif %}
    </li>
  {% endfor %}
</ul>
