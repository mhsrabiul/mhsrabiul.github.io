---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

# Ongoing Research

{% assign ongoing_research = site.research | where: "status", "ongoing" %}
{% if ongoing_research.size > 0 %}
  <ul class="research-page-content">
    {% for post in ongoing_research %}
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
  <p>No ongoing research at the moment.</p>
{% endif %}

# Finished Projects

{% assign finished_research = site.research | where: "status", "completed" %}
{% if finished_research.size > 0 %}
  <ul class="research-page-content">
    {% for post in finished_research %}
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
  <p>No finished research projects.</p>
{% endif %}

