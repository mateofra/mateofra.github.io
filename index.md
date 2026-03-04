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
          <div style="display: flex; justify-content: center; align-items: center; gap: 10px; margin-bottom: 5px;">
            <a class="song-title blink" href="{{ site.baseurl }}{{ file.path }}" style="margin-bottom: 0;">♬ {{ file.basename }} ♬</a>
            <a href="https://soundcloud.com/cheese-76336542/cheese_dentro_de_ti" target="_blank" style="color: #FF6600; font-weight: bold; text-shadow: 1px 1px #000; font-size: 0.9em; text-decoration: none;">[SoundCloud]</a>
          </div>
          <audio controls class="retro-audio">
            <source src="{{ site.baseurl }}{{ file.path }}" type="audio/mpeg">
            Tu navegador no soporta el audio.
          </audio>
        </div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
