---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order. 
nav: true
nav_order: 2
---

{% include bib_search.liquid %}

<div class="publications">

  {% bibliography --query @article[category=published] %}

  <h2 class="category" style="margin-top: 3.5rem;">Preprints & Under Review</h2>
  {% bibliography --query @article[category=preprint] %}

</div>

<style>
  /* 1. Style the category section headers to match tab titles exactly */
  .publications h2.category {
    display: block !important;
    font-size: 1.25rem !important; 
    font-weight: 500 !important;   
    color: var(--global-text-color) !important; 
    text-transform: none !important;
    letter-spacing: normal !important;
    margin-bottom: 1.5rem !important;
    padding-left: 1.5rem !important; 
  }

  /* 2. Strip right-float properties from the large year block and align left */
  .publications ol.bibliography h2.year {
    display: block !important;
    text-align: left !important;
    float: none !important;
    clear: both !important;
    position: relative !important;
    right: auto !important;
    left: 0 !important;
    font-size: 2.2rem !important; 
    font-weight: 700 !important;
    color: var(--global-text-color-light) !important; 
    opacity: 0.25 !important; 
    margin-top: 1rem !important;
    margin-bottom: 0.2rem !important;
    border-top: none !important;
    border-bottom: 1px solid var(--global-divider-color) !important;
    padding-bottom: 0.1rem !important;
    padding-left: 1.5rem !important; 
  }

  /* 3. Drop the grid structure and pull rows to full width */
  .publications .bibliography .row {
    display: block !important; 
    width: 100%;
    margin: 0 0 1.5rem 0 !important;
  }

  /* 4. Hide the leftover empty abbreviation column grid spacing */
  .publications .bibliography .row .col-sm-2 {
    display: none !important;
  }
  
  /* 5. DOUBLED HORIZONTAL SHIFT: Deepens the indentation of paper entries */
  .publications .bibliography .row .col-sm-8 {
    max-width: 100% !important;
    flex: 0 0 100% !important;
    padding-left: 3.5rem !important; /* Increased to 3.5rem for a stronger step-in look */
    padding-right: 0px !important;
    margin-top: -0.25rem !important; 
  }

  /* 6. Hide the individual entry abbreviation badges completely */
  .publications .bibliography .abbr {
    display: none !important;
  }
</style>
