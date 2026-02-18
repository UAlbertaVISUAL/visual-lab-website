---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

Welcome to the VISUAL Lab research page.

{% include section.html %}

## Highlighted

{% include list.html data="citations" component="citation" filters="featured:true" %}

{% include section.html %}

## All

{% include search-box.html %}

{% include search-info.html %}

{% include list.html 
   data="citations" 
   component="citation" 
   filters="dr-ray:true" 
%}