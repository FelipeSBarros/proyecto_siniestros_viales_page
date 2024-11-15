---
layout: page
permalink: /proyectos/siniestros_viales_misiones/
---
<div class="conteudo">
  <!-- Apresentar os objetivos -->
  <section id="objetivos">
    <h2>Objetivos del Proyecto</h2>
    <p>{{ site.data.siniestros_viales_misiones.objetivos | markdownify }}</p>
  </section>

  <!-- Apresentar a metodologia -->
  <section id="metodologia">
    <h2>Metodología</h2>
    <p>{{ site.data.siniestros_viales_misiones.metodologia | markdownify }}</p>
  </section>

  <!-- Apresentar publicações -->
  <section id="publicaciones">
    <h2>Publicaciones</h2>
    <ul>
      {% for publicacion in site.data.siniestros_viales_misiones.publicaciones %}
        <li>
          <strong>{{ publicacion.titulo }}</strong>
          {% if publicacion.documento %}
            - <a href="{{ site.baseurl }}/assets/publicaciones/{{ publicacion.documento }}" target="_blank">Descargar documento</a>
          {% endif %}
        {% if publicacion.link_dato %}
            - <a href="{{ site.baseurl }}/assets/datos/{{ publicacion.link_dato }}" target="_blank">Descargar datos</a>
          {% endif %}
        {% if publicacion.mapa_web %}
            - <a href="{{ site.baseurl }}/proyectos/siniestros_viales/{{ publicacion.mapa_web }}" target="_blank">Mapa iteractivo</a>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  </section>

  <!-- Apresentar noticias -->
  <section id="noticias">
    <h2>Noticias</h2>
    {% for noticia in site.data.siniestros_viales_misiones.noticias %}
    <div class="noticia">
      <strong>
        <ul><li><a href="{{ noticia.link }}" target="_blank">{{ noticia.titulo }}</a> ({{noticia.medio}})</li></ul>
      </strong> 
    </div>
  {% endfor %}
    </section>

  <!-- Apresentar a equipe -->
  <section id="equipe">
    <h2>Equipo del Proyecto</h2>
    <div class="equipe-container">
      {% for membro in site.data.siniestros_viales_misiones.equipo %}
        <div class="membro">
          <img src="{{ site.baseurl }}/assets/img/equipo/{{ membro.foto }}" alt="Foto de {{ membro.nome }}" class="imagem-redonda">
          <h3>{{ membro.nome }}</h3>
          <p><strong>Cargo: </strong>{{ membro.cargo }}</p>
          {% if membro.proyecto %}
            <p><strong>Proyecto: </strong>{{ membro.proyecto }}</p>
          {% endif %}
          <p>{{ membro.bio }}</p>
          {% if membro.link %}
            <a href="{{ membro.link }}" target="_blank">Página pessoal</a>
          {% endif %}
        </div>
      {% endfor %}
    </div>