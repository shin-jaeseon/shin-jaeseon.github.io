---
layout: page
title: Blog
permalink: /blog/
---

<div class="blog">
  <h1 class="page-heading">Blog</h1>

  {%- if site.posts.size > 0 -%}
    <ul class="post-list">
      {%- for post in site.posts -%}
      <li>
        <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
        <div class="post-tags">
          {%- for tag in post.tags -%}
            <a class="tag" href="/tags/{{ tag | slugify }}">{{ tag }}</a>
          {%- endfor -%}
        </div>
      </li>
      {%- endfor -%}
    </ul>
  {%- endif -%}
</div>
