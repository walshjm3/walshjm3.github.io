---
layout: default
title: Home
---

<p>Hello! I am a Ph.D. student in Business Economics at Harvard, where I was supported by the <a href="https://www.nsfgrfp.org/" rel="external nofollow noopener" target="_blank">NSF Graduate Research Fellowship</a> and am affiliated with the <a href="https://caps.gov.harvard.edu/" rel="external nofollow noopener" target="_blank">Center for American Political Studies</a>. My research fields are industrial organization and financial economics.</p>


<p><b>I am on the 2026-2027 job market.</b></p>


<p>I graduated from Harvard with an A.B. in Physics &amp; Mathematics. Before starting my Ph.D., I was a management consultant at <a href="https://www.bain.com/" rel="external nofollow noopener" target="_blank">Bain &amp; Company</a>.</p>

## Job Market Paper

<ol class="paper-list" style="list-style: none;">
  <li>
    <strong><span class="paper-title">Capital Regulation as a Barrier to Bank Consolidation</span></strong>
    (with Nathan Kaplan)
    <span class="paper-info">[Draft coming soon!]</span>
  </li>
</ol>

## Working Papers

<ol class="paper-list">
 {% assign sorted_works = site.working %}
  {% for paper in sorted_works %}
  <li>
    <strong>
      <a href="{{ paper.link }}" target="_blank" rel="noopener" class="paper-title">
        {{ paper.title }}</a></strong>
    {% if paper.authors %}
      (with {{ paper.authors }})
    {% endif %}
    {% if paper.ssrn %}
      [<a href="{{ paper.ssrn }}" target="_blank" rel="noopener" class="paper-link">SSRN</a>]
    {% endif %}
    {% if paper.info %}
      <span class="paper-info{% if paper.info_blue %} paper-info--blue{% endif %}">{{ paper.info }}</span>
    {% endif %}
    {% if paper.badge or paper.badge_date or paper.year %}
    <span class="paper-badge">{% if paper.badge %}{{ paper.badge }}{% if paper.badge_date %} · {% endif %}{% endif %}{% if paper.badge_date %}<strong>{{ paper.badge_date }}</strong>{% endif %}{% if paper.year %} {{ paper.year }}{% endif %}</span>
    {% endif %}
    {% if paper.abstract %}
    <br>
    <a 
       class="abstract-toggle d-inline-flex align-items-center collapsed"
       data-toggle="collapse"
       href="#collapse-{{ paper.id | remove: '/working/' }}"
       role="button"
       aria-expanded="false"
       aria-controls="collapse-{{ paper.id | remove: '/working/' }}"
    ><i class="fas fa-caret-right"></i> Abstract</a>
    <div class="abstract-text collapse ml-4 mb-3" id="collapse-{{ paper.id | remove: '/working/' }}">
      <p>{{ paper.abstract }}</p>
    </div>
    {% endif %}
  </li>
  {% endfor %}
</ol>

## Publications

<ol class="paper-list">
  {% assign sorted_pubs = site.publications | sort: 'id' | reverse %}
  {% for paper in sorted_pubs %}
  <li>
    <strong>
      <a href="{{ paper.link }}" target="_blank" rel="noopener" class="paper-title">
        {{ paper.title }}</a></strong>
    {% if paper.authors %}
      {% assign author_list = paper.authors | split: ", " %}
      {% if author_list.size > 20 %}
        (with {{ author_list[0] }} et al.)
      {% else %}
        (with {{ paper.authors }})
      {% endif %}
    {% endif %}
    <br>
    {% if paper.journal %}
      <span class="paper-journal"><em>{{ paper.journal }}</em>{% if paper.volume %}, {{ paper.volume }}{% if paper.issue %}({{ paper.issue }}){% endif %}{% endif %}{% if paper.year %}, {{ paper.year }}{% endif %}</span>
    {% endif %}
    <br>
  </li>
  {% endfor %}
</ol>
