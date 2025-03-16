---
layout: page
permalink: /
title: home
nav: true
nav_order: 1
---

# Publications

<div class="publications">
  <h2>Published Papers</h2>
  {% bibliography -f {{ site.scholar.bibliography }} --group_by none --query @article[selected=true] %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const publications = document.querySelectorAll('.publication');
  
  publications.forEach(pub => {
    const title = pub.querySelector('.title');
    const abstract = pub.querySelector('.abstract');
    
    if (abstract) {
      abstract.style.display = 'none';
      title.style.cursor = 'pointer';
      
      // Add toggle arrow
      const arrow = document.createElement('span');
      arrow.className = 'toggle-arrow';
      arrow.innerHTML = '▼';
      title.appendChild(arrow);
      
      title.addEventListener('click', function() {
        const isVisible = abstract.style.display === 'block';
        abstract.style.display = isVisible ? 'none' : 'block';
        arrow.innerHTML = isVisible ? '▼' : '▶';
      });
    }
  });
});
</script>

<style>
.publication .title {
  cursor: pointer;
  color: #0366d8;
  display: flex;
  align-items: center;
  gap: 8px;
}

.publication .title:hover {
  text-decoration: underline;
}

.publication .toggle-arrow {
  font-size: 0.8em;
  color: #666;
  transition: transform 0.2s ease;
}

.publication .abstract {
  margin-top: 10px;
  padding: 10px;
  background-color: #f6f8fa;
  border-radius: 4px;
}
</style> 