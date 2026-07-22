---
layout: default
title: Home
---

<p>I am a Ph.D. student in Business Economics at Harvard, where I was supported by the <a href="https://www.nsfgrfp.org/" rel="external nofollow noopener" target="_blank">NSF Graduate Research Fellowship</a> and am affiliated with the <a href="https://caps.gov.harvard.edu/" rel="external nofollow noopener" target="_blank">Center for American Political Studies</a>.</p>


<p><b>I am on the 2026-2027 job market.</b></p>


<p>I graduated from Harvard with an A.B. in Physics &amp; Mathematics. Before starting my Ph.D., I was a management consultant at <a href="https://www.bain.com/" rel="external nofollow noopener" target="_blank">Bain &amp; Company</a>.</p>

## Job Market Paper

<ol class="paper-list" style="list-style: none;">
  <li>
    <strong><span class="paper-title" style="color: var(--global-theme-color);">Mergers with Regulated Capital.</span></strong>
    <span class="paper-info">[Draft coming soon!]</span>
    <br>
    with Nathan Kaplan
  </li>
</ol>

## Working Papers

<ol class="paper-list">
 {% assign sorted_works = site.working | sort: 'id' | reverse %}
  {% for paper in sorted_works %}
  <li>
    <strong>
      <a href="{{ paper.link }}" target="_blank" rel="noopener" class="paper-title">
        {{ paper.title }}.
      </a>
    </strong>
    {% if paper.ssrn %}
      [<a href="{{ paper.ssrn }}" target="_blank" rel="noopener" class="paper-link">SSRN</a>]
    {% endif %}
    {% if paper.authors %}
    <br>
      with {{ paper.authors }}
    {% endif %}
    {% if paper.info %}
      <span class="paper-info{% if paper.info_blue %} paper-info--blue{% endif %}">{{ paper.info }}</span>
    {% endif %}
    {% if paper.badge or paper.badge_date or paper.year %}
    <br>
    <span class="paper-badge">{% if paper.badge %}{{ paper.badge }}{% if paper.badge_date %} · {% endif %}{% endif %}{% if paper.badge_date %}<strong>{{ paper.badge_date }}</strong>{% endif %}{% if paper.year %} {{ paper.year }}{% endif %}</span>
    {% endif %}
    {% if paper.abstract %}
    <br>
    <a 
       class="d-inline-flex align-items-center collapsed" 
       style="color: black; text-decoration: none; cursor: pointer;"
       data-toggle="collapse"
       href="#collapse-{{ paper.id | remove: '/working/' }}"
       role="button"
       aria-expanded="false"
       aria-controls="collapse-{{ paper.id | remove: '/working/' }}"
    >
      <i class="fas fa-caret-right mr-1"></i> Abstract
    </a>
    <div class="collapse ml-4 mb-3" id="collapse-{{ paper.id | remove: '/working/' }}">
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
        {{ paper.title }}.
      </a>
    </strong>
    {% if paper.authors %}
     <br>
      with {{ paper.authors }}
    {% endif %}
    <br>
    {% if paper.journal %}
      <em>{{ paper.journal }}</em>, <em>{{ paper.year }}</em>
    {% endif %}
    <br>
  </li>
  {% endfor %}
</ol>
