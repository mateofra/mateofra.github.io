---
layout: default
title: Test
---

## Bienvenid@ a mi pagina en la Web  
Me llamo Mateo (como la URL indica) y estudio inteligencia artificial en la USC.  

![Alien Glow](/img/alien.gif)
![Under Construction](/img/construction.gif)

Aquí subiré "artículos", como si de un diario se tratase. ↴  
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Música
<ul class="music-list">
  {% for file in site.static_files %}
    {% if file.path contains '/music/' and file.extname == '.mp3' %}
      <li class="music-track">
        <div class="player-container">
          <a class="song-title blink" href="{{ site.baseurl }}{{ file.path }}">♬ {{ file.basename }} ♬</a>
          <audio controls class="retro-audio">
            <source src="{{ site.baseurl }}{{ file.path }}" type="audio/mpeg">
            Tu navegador no soporta el audio.
          </audio>
        </div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
