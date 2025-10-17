---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

## Working papers and work in progress

{% for paper in site.research reversed %}
  <div class="research-item" style="margin-bottom: 2em;">
    <h3 style="margin-bottom: 0.5em;">{{ paper.title }}</h3>
    
    {% if paper.authors %}
    <p style="color: #666; margin: 0.5em 0;">with {{ paper.authors }}</p>
    {% endif %}
    
    {% if paper.abstract %}
    <details style="margin-top: 1em;">
      <summary style="cursor: pointer; color: var(--link-color, #0066cc); font-weight: 500;">Abstract</summary>
      <div style="margin-top: 1em; padding-left: 1em; border-left: 3px solid #eee;">
        {{ paper.abstract }}
      </div>
    </details>
    {% endif %}
    
    {% if paper.pdf or paper.slides or paper.link %}
    <p style="margin-top: 1em;">
      {% if paper.pdf %}<a href="{{ paper.pdf | prepend: base_path }}" style="margin-right: 1em;">[PDF]</a>{% endif %}
      {% if paper.slides %}<a href="{{ paper.slides | prepend: base_path }}" style="margin-right: 1em;">[Slides]</a>{% endif %}
      {% if paper.link %}<a href="{{ paper.link }}" style="margin-right: 1em;">[Link]</a>{% endif %}
    </p>
    {% endif %}
  </div>
{% endfor %}
