---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<h2>Ongoing Research</h2>
{% assign ongoing_posts = site.research.ongoing %}
{% if ongoing_posts.size > 0 %}
  <ul class="research-page-content">
    {% for post in ongoing_posts %}
      <li class="research-post-content">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.abstract }}</p>
        {% if post.image %}
          <p>Image Path: {{ post.image }}</p>  <!-- Debugging line -->
          <img src="{{ site.baseurl }}{{ post.image }}" alt="{{ post.title }}" class="research-post-image">
        {% endif %}
        <p><a href="{{ post.url }}">Read more</a></p>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No ongoing research posts available.</p>
{% endif %}

<h2>Completed Projects</h2>
{% assign completed_posts = site.research.completed %}
{% if completed_posts.size > 0 %}
  <ul class="research-page-content">
    {% for post in completed_posts %}
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
  <p>No completed projects available.</p>
{% endif %}

