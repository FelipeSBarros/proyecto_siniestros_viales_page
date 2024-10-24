---
layout: page
#title: Publicaciones
#permalink: /publicaciones/
---

<ul>
  {% for file in site.static_files %}
    {% if file.publicacion %}
      <li>
        <a href="{{ site.baseurl }}{{ file.path }}" target="_blank">{{ file.name }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>