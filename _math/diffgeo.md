---
title: "Differential Geometry"
date: 2026-06-29
---

Do Carmo book

{% assign weeks = site.progress | sort: "date" | reverse %}
{% for week in weeks %} {% if week.diff_geo_entries %}
{% for entry in week.diff_geo_entries %}

## {{ entry.date }}

{{ entry.summary }}  
From: [{{ week.title }}]({{ site.baseurl }}{{ week.url }})

<div style="display: flex; gap: 10px; flex-wrap: wrap;">
  {% for image in entry.images %}
  <img src="{{ site.baseurl }}{{ image }}" alt="Differential geometry notes" style="flex: 1; min-width: 200px; width: 0; height: auto;">
  {% endfor %}
</div>
    {% endfor %}
  {% endif %}
{% endfor %}
