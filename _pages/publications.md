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

  <h2 class="category">Published Journal Articles</h2>
  {% bibliography --query @article[category=published] %}

  <h2 class="category" style="margin-top: 2.5rem;">Preprints & Under Review</h2>
  {% bibliography --query @article[category=preprint] %}

</div>

<!-- Custom style to turn the numbering badges into plain text -->
<style>
  .publications abbr.badge {
    background-color: transparent !important;
    color: var(--global-text-color) !important;
    border: none !important;
    padding: 0 !important;
    font-size: 1.1rem !important;
    font-weight: 500;
    box-shadow: none !important;
  }
</style>
