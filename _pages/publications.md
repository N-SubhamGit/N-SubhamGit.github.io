---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order. 
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->
{% include bib_search.liquid %}

<div class="publications">

  <h2 class="category">Published Papers</h2>
  {% bibliography --query @article, @inproceedings %}

  <h2 class="category" style="margin-top: 2rem;">Preprints & Working Papers</h2>
  {% bibliography --query @unpublished %}

</div>
