---
layout: page
permalink: /publications/
title: Publications
description:
sections:
  - bibquery: "@inproceedings"
    text: "Conference"
  - bibquery: "@article"
    text: "Journal"
  - bibquery: "@techreport"
    text: "Technical Report"
  - bibquery: "@report"
    text: "Preprint"
  - bibquery: "@misc"
    text: "Thesis"
years: [2032, 2031, 2030, 2029, 2028, 2027, 2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019]
nav: false
social: true
nav_order: 3
---

<div class="publications">

{%- for section in page.sections %}
  <a id="{{section.text}}"></a>
  <h3 class="bibtitle">{{section.text}}</h3>
  {%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      <h3 class="year">{{y}}</h3>
      {% bibliography -f {{site.scholar.bibliography}} -q {{section.bibquery}}[year={{y}}] %}

    {%- endif -%}

  {%- endfor %}

{%- endfor %}

</div>
