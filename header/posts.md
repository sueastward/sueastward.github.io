---
layout: default
title: 日志
permalink: /Posts
---
{%- if site.posts.size > 0 -%}
<ul class="post-list">
  {%- for post in site.posts -%}
  <li>
    <h3 class="posts-title">
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    <span class="post-meta">{{ post.date | date: "%F" }}</span>
  </li>
  {%- endfor -%}
</ul>
{%- endif -%}