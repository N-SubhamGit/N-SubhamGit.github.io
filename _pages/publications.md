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

<!-- Custom CSS to display the year cleanly on the left and fix margins -->
<style>
  /* 1. Style the year badge text on the left */
  .publications abbr.badge {
    background-color: transparent !important;
    color: #f0f0f0 !important; /* Clearly visible light text */
    border: none !important;
    padding: 0 !important;
    font-size: 1.1rem !important;
    font-weight: 600 !important;
    box-shadow: none !important;
    text-align: left;
    display: inline-block;
  }

  /* 2. Set an optimal width for the left year column so it doesn't clip */
  .publications .bibliography .row .col-sm-2 {
    max-width: 12% !important;
    flex: 0 0 12% !important;
    padding-right: 10px !important;
  }

  /* 3. Expand the title text section to comfortably use the rest of the row */
  .publications .bibliography .row .col-sm-8 {
    max-width: 88% !important;
    flex: 0 0 88% !important;
    padding-left: 0px !important;
  }
  
  /* 4. Optional: Hide the default large faint year on the right if it feels redundant */
  .publications .periodical {
    /* uncomment the line below if you want to remove the faint year on the far right */
    /* display: none !important; */
  }
</style>
