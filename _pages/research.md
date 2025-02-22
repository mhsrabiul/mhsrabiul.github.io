---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<h2>Ongoing Research</h2>
<ul class="research-page-content">
  {% for post in site.research.ongoing %}
    <li class="research-post-content">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.abstract }}</p>
      {% if post.image %}
        <img src="{{ post.image }}" alt="{{ post.title }}">
      {% endif %}
      <p><a href="{{ post.url }}">Read more</a></p>
    </li>
  {% endfor %}
</ul>

<h2>Completed Projects</h2>
<ul class="research-page-content">
  {% for post in site.research.completed %}
    <li class="research-post-content">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.abstract }}</p>
      {% if post.image %}
        <img src="{{ post.image }}" alt="{{ post.title }}">
      {% endif %}
      <p><a href="{{ post.url }}">Read more</a></p>
    </li>
  {% endfor %}
</ul>