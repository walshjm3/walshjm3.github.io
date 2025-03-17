---
layout: default
title: Home
---

<p>I am a Ph.D. student in Business Economics at Harvard, where I am supported by the <a href="https://www.nsfgrfp.org/" rel="external nofollow noopener" target="_blank">NSF Graduate Research Fellowship</a> and <a href="https://opportunityinsights.org/" rel="external nofollow noopener" target="_blank">Opportunity Insights</a>.</p>

<p>I graduated from Harvard with an A.B. in Physics &amp; Mathematics. Before starting my Ph.D., I was a management consultant at <a href="https://www.bain.com/" rel="external nofollow noopener" target="_blank">Bain &amp; Company</a> and a research assistant at the <a href="https://www.nber.org/" rel="external nofollow noopener" target="_blank">National Bureau of Economic Research</a> for Professor Claudia Goldin. Before economics, I did research in computational biology.</p>

<p>My research studies agency frictions and their impacts on financial markets, using tools from public finance, industrial organization, and econometrics.</p>

## Working Papers

{% for paper in site.publications %}
<p>
  <a class="btn btn-link"
     data-toggle="collapse"
     href="#{{ paper.id }}"
     role="button"
     aria-expanded="false"
     aria-controls="{{ paper.id }}">
    <strong>{{ paper.title }}</strong>
    {% if paper.coauthors %}
      <em>, {{ paper.coauthors }}</em>
    {% endif %}
  </a>
</p>

<div class="collapse" id="{{ paper.id }}">
  <p>{{ paper.abstract }}</p>
  {% if paper.link %}
    <p>
      <a href="{{ paper.link }}" target="_blank" rel="noopener">
        Read Online
      </a>
    </p>
  {% endif %}
</div>
{% endfor %}
