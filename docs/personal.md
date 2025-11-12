---
title: Personal Blog
layout: page
permalink: /personal/
---

### Posts
<ul class="post-list">
  {%- assign personal_posts = site.categories.personal | sort: "date" | reverse -%}
  {%- for post in personal_posts -%}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-meta">{{ post.date | date: "%-d %b %Y" }}</span>
      {%- if post.excerpt -%}<p>{{ post.excerpt }}</p>{%- endif -%}
    </li>
  {%- endfor -%}
</ul>