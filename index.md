---
layout: home
title: Compass - Information Security Manual
---

<div class="manual-home">
  <h1>Information Security Manual</h1>
  
  <p class="manual-intro">
    Welcome to our Information Security Manual. This comprehensive resource contains all the policies, procedures, and guides that govern our information security practices.
  </p>

  <div class="manual-sections">
    <div class="section-card">
      <h2>Policies</h2>
      <p>Formal statements that define our organization's rules and guidelines for information security.</p>
      <ul>
        {% for page in site.pages %}
          {% if page.path contains 'Policies/' and page.title %}
            <li>
              <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
              {% if page.document_id %}<span class="doc-id">{{ page.document_id }}</span>{% endif %}
            </li>
          {% endif %}
        {% endfor %}
      </ul>
      <a href="{{ '/policies/' | relative_url }}" class="view-all">View all policies →</a>
    </div>

    <div class="section-card">
      <h2>Procedures</h2>
      <p>Step-by-step instructions for implementing our security policies and performing security-related tasks.</p>
      <ul>
        {% for page in site.pages %}
          {% if page.path contains 'Procedures/' and page.title %}
            <li>
              <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
              {% if page.document_id %}<span class="doc-id">{{ page.document_id }}</span>{% endif %}
            </li>
          {% endif %}
        {% endfor %}
      </ul>
      <a href="{{ '/procedures/' | relative_url }}" class="view-all">View all procedures →</a>
    </div>

    <div class="section-card">
      <h2>Guides</h2>
      <p>Helpful resources and best practices for maintaining information security.</p>
      <ul>
        {% for page in site.pages %}
          {% if page.path contains 'Guides/' and page.title %}
            <li>
              <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
              {% if page.document_id %}<span class="doc-id">{{ page.document_id }}</span>{% endif %}
            </li>
          {% endif %}
        {% endfor %}
      </ul>
      <a href="{{ '/guides/' | relative_url }}" class="view-all">View all guides →</a>
    </div>
  </div>
</div> 