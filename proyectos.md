---
layout: page
title: Proyectos
permalink: /proyectos/
---

<div class="">
    {% for proyecto in site.data.proyectos %}
        <div class="">
            <a href="{{ site.baseurl }}/{{proyecto.enlace}}">
                <h3>{{ proyecto.nome }}</h3>
            </a>
        </div>
    {% endfor %}
</div>
