---
title: Presentations
feature_text: |
 ## Presentations
excerpt: "Presentations"

---

{% for batch in site.data.presentations %}

  <h1>{{ batch.year }}</h1>

  <div class="csl-bib-body" style="line-height: 1.35; margin-left: 2em; margin-top: 1em; margin-bottom: 2em; text-indent:-2em;">

  {% for paper in batch.presentations %}
      <div class="csl-entry" style="margin-bottom: 1em;">{{ paper.citation }}
      {% if paper.links %}[{% for link in paper.links %}<a href="{{ link.href }}" style="color: #2B599E;">{{ link.label }}</a>{% if forloop.last == false %}, {% endif %}{% endfor %}]{% endif %}</div>
  {% endfor %}
  
  </div>
{% endfor %}