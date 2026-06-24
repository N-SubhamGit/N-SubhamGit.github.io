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

  <h2 class="category">Published Journal Articles</h2>
  {% bibliography --query @article[category=published] %}

  <h2 class="category" style="margin-top: 2.5rem;">Preprints & Under Review</h2>
  {% bibliography --query @article[category=preprint] %}

</div>
