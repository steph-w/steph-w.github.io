---
layout: page
title: Publications
permalink: publications/
---

<p class="pub-caption">* indicates equal contribution</p>

<div class="pub-list">
{% assign grouped = site.data.publications | group_by: "category" %}
{% for group in grouped %}
  <div class="pub-category">
    <h5>{{ group.name }}</h5>
    <div class="pub-category-group">
    {% for article in group.items %}
      {% include publication-item.html article=article %}
    {% endfor %}
    </div>
  </div>
{% endfor %}
</div>
