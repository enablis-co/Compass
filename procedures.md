---
layout: page
title: Procedures
permalink: /procedures/
---

# Procedures

These procedures provide step-by-step instructions for common tasks.

<ul class="document-list">
{% for page in site.pages %}
  {% if page.path contains 'Procedures/' and page.title %}
    <li>
      <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
      {% if page.document_id %}- {{ page.document_id }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul> 