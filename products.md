---
layout: page
title: Products
permalink: /products/
---

<div class="ps__home">
  <ul class="ps__posts">
    {% for post in site.categories.product %}
    <li class="ps__posts__item">
      <figure>
        {% if post.featured-image %}
          <img src="{{ post.featured-image | prepend: site.baseurl }}" alt="{{ post.title }}">
        {% else %}
          <img src="images/feature_placeholder.jpg" alt="{{ post.title }}">
        {% endif %}
        <a href="{{ post.url | prepend: site.baseurl }}">
        <figcaption> {{ post.title }} </figcaption>
        </a>
      </figure>
    </li>
    {% endfor %}
  </ul>
