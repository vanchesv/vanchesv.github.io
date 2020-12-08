---
layout: default
title: Publicaciones
description: Accede a todas las publicaciones de EGHYA
---

# Archivos

> En esta sección puedes acceder a todas las publicaciones ordenadas por mes y año.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h2>{{ yearMonth.name }}</h2>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
