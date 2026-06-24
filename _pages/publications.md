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

<!-- Custom CSS to make numbers visible and reduce the massive left margin gap -->
<style>
  /* 1. Make the plain text numbers clearly visible against the dark background */
  .publications abbr.badge {
    background-color: transparent !important;
    color: #f0f0f0 !important; /* Force a clear white/light gray color */
    border: none !important;
    padding: 0 !important;
    font-size: 1.15rem !important;
    font-weight: 600 !important;
    box-shadow: none !important;
    text-align: right;
    display: inline-block;
    width: 100%;
  }

  /* 2. Drastically shrink the width allocation for the left column (numbers/abbr column) */
  .publications .bibliography .row .col-sm-2 {
    max-width: 5% !important;
    flex: 0 0 5% !important;
    padding-right: 0px !important;
    margin-right: 10px !important;
  }

  /* 3. Expand the right column (the paper text) to fill up the reclaimed space */
  .publications .bibliography .row .col-sm-8 {
    max-width: 90% !important;
    flex: 0 0 90% !important;
    padding-left: 5px !important;
  }
</style>
