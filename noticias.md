---
layout: page
title: Noticias
permalink: /noticias/
---

<div class="">
  {% for noticia in site.data.noticias %}
  <div class="social-media-list">
    <h3>{{ noticia.medio }}</h3>
        <a href="{{ noticia.link }}" target="_blank"><strong>{{ noticia.titulo }}</strong>
            {% if noticia.youtube %}
                <li><a href="{{ noticia.youtube | escape }}" target="_blank">
                <svg class="svg-icon">
                    <use xlink:href="{{ '/assets/minima-social-icons.svg#youtube' | relative_url }}"></use>
                </svg></a></li>
            {% endif %}
        </a>
    </div>
  {% endfor %}
</div>
