---
layout: page
title: Índice de entradas
permalink: /indice/
---

<a>{{ site.tags.TAG }}</a>

<ul class="minimal">
{% for post in site.posts %}
  <li>
    {{ post.date | date: "%b %d, %Y"  }} &mdash; <a href="{% if post.external_url %}{{ post.external_url }}{% else %}{{ post.url }}{% endif %}">{% if post.title != "" %}{{ post.title }}{% else %}{{ post.slug }}{% endif %}</a>
  </li>
{% endfor %}
</ul>
