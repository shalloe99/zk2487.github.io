---
layout: page
permalink: /research/
title: research
description: Research Papers and Presentations
years: [1956, 1950, 1935, 1905]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
