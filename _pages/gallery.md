---
layout: page
permalink: /gallery/
title: gallery
description: My art gallery.
nav: true
display_categories: [reflection, fantasy, nature]
horizontal: false
---

Artists are simple people with the complex mind ≠ Simple people with a complex mind are artists

<div class="projects">
 {% if site.enable_gallery_categories and page.display_categories %}
   <!-- Display categorized projects -->
    {% for category in page.display_categories %}
      <h2 class="category">{{ category }}</h2>
      {% assign categorized_gallery = site.gallery | where: "category", category %}
      {% assign sorted_gallery = categorized_gallery | sort: "importance" %}
      <!-- Generate cards for each project -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-2">
          {% for project in sorted_gallery %}
            {% include projects_horizontal.html %}
          {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for project in sorted_gallery %}
            {% include projects.html %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}


    {% else %}
  <!-- Display projects without categories -->
    {% assign sorted_gallery = site.gallery | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-2">
        {% for gallery in sorted_gallery %}
          {% include projects_horizontal.html %}
        {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for gallery in sorted_gallery %}
          {% include projects.html %}
        {% endfor %}
      </div>
    {% endif %}

  {% endif %}
</div>