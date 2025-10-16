---
layout: page
title: Research
permalink: /research/
---

## Working papers and work in progress

{% for paper in site.research %}
<div class="research-item" style="margin-bottom: 2.5em;">

### {{ paper.title }}

{% if paper.authors %}
<p style="color: #666; margin-top: 0.5em;">
with {{ paper.authors }}
</p>
{% endif %}

{% if paper.abstract %}
<details style="margin-top: 1em;">
<summary style="cursor: pointer; color: #0066cc; font-weight: 500;">▼ Abstract</summary>
<div style="margin-top: 1em; padding-left: 1em; border-left: 3px solid #eee;">
{{ paper.abstract }}
</div>
</details>
{% endif %}

{% if paper.pdf %}
<p style="margin-top: 1em;">
<a href="{{ paper.pdf }}" style="color: #0066cc;">[PDF]</a>
</p>
{% endif %}

</div>
{% endfor %}
