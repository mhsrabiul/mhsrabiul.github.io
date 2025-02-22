---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

# Research

{% assign research_posts = site.research %}
{% if research_posts.size > 0 %}
  <ul class="research-page-content">
    {% for post in research_posts %}
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
{% else %}
  <p>No research posts available.</p>
{% endif %}
