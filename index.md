---
layout: home
title: Security Framework @ Enablis
---

<div class="manual-home">
  
  <p class="manual-intro">
    Welcome to our Information Security Manual. This comprehensive resource contains all the policies, procedures, and guides that govern our information security practices.
  </p>

  <div class="manual-sections">
    <div class="section-card">
      <h2>ISMS Manual</h2>
      <p>Start here with our Information Security Management System (ISMS) Manual - the primary navigational document for our security framework.</p>
      <a href="{{ '/isms-manual/' | relative_url }}" class="view-all">Read the ISMS Manual →</a>
      <br>
    </div>

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
    </div>
  </div>
</div>
