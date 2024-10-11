---
layout: page
title: Equipo
permalink: /el_equipo/
---

<div class="equipe-container">
  {% for membro in site.data.equipo %}
  <div class="membro">
    <img src="{{ site.baseurl }}/assets/img/equipo/{{ membro.foto }}" alt="Foto de {{ membro.nome }}" class="imagem-redonda">
    <h3>{{ membro.nome }}</h3>
    <p><strong>{{ membro.cargo }}</strong></p>
    <p>{{ membro.bio }}</p>
    {% if membro.link %}
        <a href="{{ membro.link }}" target="_blank">Página pessoal</a>
    {% endif %}
  </div>
  {% endfor %}
</div>
