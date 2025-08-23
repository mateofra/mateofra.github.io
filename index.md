---
layout: default
title: Test
---

<h1>Testing</h1>
<p>If you see this, markdown and theme are working.</p>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
