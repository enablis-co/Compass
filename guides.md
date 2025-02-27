---
layout: page
title: Guides
permalink: /guides/
---

## Guides

These guides provide helpful information and best practices.

<ul class="document-list">
{% for page in site.pages %}
  {% if page.path contains 'Guides/' and page.title %}
    <li>
      <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
      {% if page.document_id %}- {{ page.document_id }}{% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>
