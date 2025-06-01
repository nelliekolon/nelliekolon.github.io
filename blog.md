---
layout: default
title: Blog
---

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <h3>{{post.date | date_to_string}}</h3>
  {% if post.image %}
  <img src="{{ post.image }}" alt="{{ post.title }}">
  {% endif %}
  <p>{{ post.excerpt }}</p>
{% endfor %}