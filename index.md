---
layout: default
title: Test
---

## Bienvenid@ a mi pagina en la Web  
Me llamo Mateo (como la URL indica) y estudio inteligencia artificial en la USC.  
Aquí subiré "artículos", como si de un diario se tratase. ↴  
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
