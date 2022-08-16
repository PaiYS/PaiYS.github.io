---
layout: page
permalink: /publications/
title: publications
description: Publications by categories in reversed chronological order. 
years: [2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
nav: true
nav_order: 1
---

* [Google Scholar](https://scholar.google.com/citations?user={{site.data.scholar.id}})
* Citations: {{ site.data.scholar.citations }}
* h-index: {{ site.data.scholar.h_index }}
* i10-index: {{ site.data.scholar.i10_index }}

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
