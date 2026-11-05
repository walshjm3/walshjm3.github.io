---
layout: default
title: Home
---

<p>Hello! I am a Ph.D. student in Business Economics at Harvard. My research fields are industrial organization and finance. I study banking, antitrust, and corporate governance.</p>


<p>I was supported by the <a href="https://www.nsfgrfp.org/" rel="external nofollow noopener" target="_blank">NSF Graduate Research Fellowship</a> and am affiliated with the <a href="https://caps.gov.harvard.edu/" rel="external nofollow noopener" target="_blank">Center for American Political Studies</a>. I graduated from Harvard with an A.B. in Physics &amp; Mathematics. Before starting my Ph.D., I was a management consultant at <a href="https://www.bain.com/" rel="external nofollow noopener" target="_blank">Bain &amp; Company</a>.</p>


<p><b>I am on the 2026-2027 job market.</b></p>


## Job Market Paper

<ol class="paper-list">
  <li>
    <strong>
      <a href="/assets/walsh_jmp.pdf" target="_blank" rel="noopener" class="paper-title">
        Capital Regulation as a Barrier to Bank Consolidation</a></strong>
    (with Nathan Kaplan)
    [<a href="/assets/walsh_jmp.pdf" target="_blank" rel="noopener" class="paper-link">PDF</a>]
    <br>
    <a 
       class="abstract-toggle d-inline-flex align-items-center collapsed"
       data-toggle="collapse"
       href="#collapse-jmp"
       role="button"
       aria-expanded="false"
       aria-controls="collapse-jmp"
    ><i class="fas fa-caret-right"></i> Abstract</a>
    <div class="abstract-text collapse ml-4 mb-3" id="collapse-jmp">
      <p>While thousands of mergers have reshaped the United States banking sector since the 1990s, the U.S. still has more banks per capita than other large countries. We show that equity capital regulation has meaningfully depressed bank M&amp;A activity by making leverage-increasing financing expensive. Using a 2001 policy change in accounting standards as an instrument for the post-merger regulatory capital of target banks, we find that a standard deviation increase in capital raises the probability of a bank being purchased within a year by approximately 50%. Estimating a structural model of banks choosing merger partners subject to capital constraints, we find that weakening capital requirements around M&amp;A since 1992 would have led to more consolidation and 19% fewer operating banks in 2022. Fixed cost efficiencies realized from additional mergers are of similar magnitude to consumer welfare losses from lower competition in deposit and loan markets. However, pairing weakened requirements with additional antitrust screening could have retained efficiencies while protecting consumer surplus.</p>
    </div>
  </li>
</ol>

## Working Papers

<ol class="paper-list">
 {% assign sorted_works = site.working %}
  {% for paper in sorted_works %}
  <li>
    <strong>
      {% if paper.link %}
      <a href="{{ paper.link }}" target="_blank" rel="noopener" class="paper-title">
        {{ paper.title }}</a>
      {% else %}
      <span class="paper-title">{{ paper.title }}</span>
      {% endif %}</strong>
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

## Works in Progress

<ol class="paper-list">
  <li>
    <strong><span class="paper-title">Merger Review by Market Definition: Evidence from Banking</span></strong>
    (with Harry Cooperman)
  </li>
  <li>
    <strong><span class="paper-title">Banking in the Town Square</span></strong>
    (with Iris Li)
  </li>
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
