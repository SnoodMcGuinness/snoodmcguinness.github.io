---
title: Technical Blog
layout: page
permalink: /tech/
---

## Project Summary
A few sentences about the technical project, goals, and scope. <!-- Add details here -->

## LLM Leaderboard
<table>
  <thead>
    <tr>
      <th>Rank</th>
      <th>Model</th>
      <th>Score</th>
      <th>Notes</th>
      <th>Date</th>
    </tr>
  </thead>
  <tbody>
  {%- assign rows = site.data.llms | sort: "score" | reverse -%}
  {%- for r in rows -%}
    <tr>
      <td>{{ forloop.index }}</td>
      <td>
        {%- if r.link -%}
          <a href="{{ r.link }}">{{ r.model }}</a>
        {%- else -%}
          {{ r.model }}
        {%- endif -%}
      </td>
      <td>{{ r.score }}</td>
      <td>{{ r.notes }}</td>
      <td>{{ r.date }}</td>
    </tr>
  {%- endfor -%}
  </tbody>
</table>

[//]: # (## Experiment Posts)

[//]: # (<ul class="post-list">)

[//]: # (  {%- assign tech_posts = site.categories.tech | sort: "date" | reverse -%})

[//]: # (  {%- for post in tech_posts -%})

[//]: # (    <li>)

[//]: # (      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>)

[//]: # (      <span class="post-meta">{{ post.date | date: "%-d %b %Y" }}</span>)

[//]: # (      {%- if post.excerpt -%}<p>{{ post.excerpt }}</p>{%- endif -%})

[//]: # (    </li>)

[//]: # (  {%- endfor -%})

[//]: # (</ul>)