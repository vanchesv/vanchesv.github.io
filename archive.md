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

***

¡Suscríbete al [boletín](https://tinyletter.com/elvanches) para recibir avisos sobre nuevas publicaciones! Tal vez recibas una sorpresa de vez en cuando...

<form style="border:1px solid #ccc;padding:3px;text-align:center;" action="https://tinyletter.com/elvanches" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/elvanches', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true"><p><label for="tlemail">Enter your email address</label></p><p><input type="text" style="width:140px" name="email" id="tlemail" /></p><input type="hidden" value="1" name="embed"/><input type="submit" value="Subscribe" /><p><a href="https://tinyletter.com" target="_blank">powered by TinyLetter</a></p></form>