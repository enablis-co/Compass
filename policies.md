---
layout: page
title: Policies
permalink: /policies/
---

## Policies

These policies establish the rules and guidelines for our organization.

<ul class="document-list">
{% for page in site.pages %}
  {% if page.path contains 'Policies/' and page.title %}
    <li>
      <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
      {% if page.document_id %}- {{ page.document_id }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>
