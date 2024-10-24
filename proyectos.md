---
layout: page
title: Proyectos
permalink: /proyectos/
---

<div class="">
  {% for proyecto in site.data.proyectos %}
  <div class="">
    <h3>{{ proyecto.nome }}</h3>
    <p><strong>Objetivos: </strong> {{ proyecto.objetivos }}</p>
    <p><strong>Metodologia: </strong> {{ proyecto.metodologia }}</p>
    {% if proyecto.publicaciones %}
        <h4>Publicaciones:</h4>
        {% for publicacion in proyecto.publicaciones %}
            <li> <p><strong>Título: </strong> <a href="{{ site.baseurl }}/assets/publicaciones/{{publicacion.documento}}" target="_blank"> {{ publicacion.titulo }} </a></p> </li>
        {% endfor %}
    {% endif %}
  </div>
  {% endfor %}
</div>
