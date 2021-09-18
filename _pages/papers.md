---
layout: page
permalink: /papers/
title: papers
description: publicaciones científicas que me parecen interesantes.
years: [2016, 1998]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
