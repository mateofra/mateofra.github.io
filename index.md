---
layout: default
title: Test
---

## Bienvenid@ a mi pagina en la Web  
Me llamo Mateo (como la URL indica) y estudio inteligencia artificial en la USC.  

![Cat typing](/img/cat_typing.gif) 
![Hackerman](/img/hackerman.gif)

Aquí subiré "artículos", como si de un diario se tratase. ↴  
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Música
<ul>
  {% for file in site.static_files %}
    {% if file.path contains '/music/' and file.extname == '.mp3' %}
      <li>
        <audio controls>
          <source src="{{ site.baseurl }}{{ file.path }}" type="audio/mpeg">
          Tu navegador no soporta el audio.
        </audio>
        <br>
        <a href="{{ site.baseurl }}{{ file.path }}">{{ file.basename }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
