---
title: Personal Blog
layout: page
permalink: /personal/
---

<ul class="post-list">
  {%- assign personal_posts = site.posts | where_exp: "p", "p.categories contains 'personal'" -%}
  {%- for post in personal_posts -%}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-meta">{{ post.date | date: "%-d %b %Y" }}</span>
      {%- if post.excerpt -%}<p>{{ post.excerpt }}</p>{%- endif -%}
    </li>
  {%- endfor -%}
</ul>