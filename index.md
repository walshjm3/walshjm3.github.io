---
layout: default
title: Home
---

<p>I am a Ph.D. student in Business Economics at Harvard, where I am supported by the <a href="https://www.nsfgrfp.org/" rel="external nofollow noopener" target="_blank">NSF Graduate Research Fellowship</a> and <a href="https://opportunityinsights.org/" rel="external nofollow noopener" target="_blank">Opportunity Insights</a>.</p>

<p>I graduated from Harvard with an A.B. in Physics &amp; Mathematics. Before starting my Ph.D., I was a management consultant at <a href="https://www.bain.com/" rel="external nofollow noopener" target="_blank">Bain &amp; Company</a> and a research assistant at the <a href="https://www.nber.org/" rel="external nofollow noopener" target="_blank">National Bureau of Economic Research</a> for Professor Claudia Goldin. Before economics, I did research in computational biology.</p>

<p>My research studies agency frictions and their impacts on financial markets, using tools from public finance, industrial organization, and econometrics.</p>

## Working Papers

{% assign sorted_works = site.working | sort: 'year' | reverse %}
{% for paper in sorted_works %}
<!-- Paper title line -->
<p>
  <strong>
    <a href="{{ paper.link }}" target="_blank" rel="noopener" style="color: black; text-decoration: none;">
      {{ paper.title }}
    </a>
  </strong>
  {% if paper.journal %}
    <em> – {{ paper.journal }}</em>
  {% endif %}
  {% if paper.authors %}
    <span> (with {{ paper.authors }})</span>
  {% endif %}
  {% if paper.year %}
    <span> – {{ paper.year }}</span>
  {% endif %}
</p>

<!-- Toggle for Abstract -->
<p>
  <a 
    class="d-inline-flex align-items-center collapsed" 
    style="color: black; text-decoration: none; cursor: pointer;"
    data-toggle="collapse"
    href="#{{ paper.id }}"
    role="button"
    aria-expanded="false"
    aria-controls="{{ paper.id }}"
  >
    Abstract <i class="fas fa-caret-right ml-1"></i>
  </a>
</p>

<!-- Collapsible abstract section -->
<div class="collapse ml-4 mb-3" id="{{ paper.id }}">
  <p>{{ paper.abstract }}</p>
</div>
{% endfor %}

## Publications

{% assign sorted_pubs = site.publications | sort: 'year' | reverse %}
{% for paper in sorted_pubs %}
<!-- Paper title line -->
<p>
  <strong>
    <a href="{{ paper.link }}" target="_blank" rel="noopener" style="color: black; text-decoration: none;">
      {{ paper.title }}
    </a>
  </strong>
  {% if paper.journal %}
    <em> – {{ paper.journal }}</em>
  {% endif %}
  {% if paper.authors %}
    <span> (with {{ paper.authors }})</span>
  {% endif %}
  {% if paper.year %}
    <span> – {{ paper.year }}</span>
  {% endif %}
</p>

{% endfor %}