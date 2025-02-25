---
layout: home
title: Enablis Policies Portal
---

<div class="home-sections">

# Enablis Policies and Documentation

Welcome to the Enablis policies and documentation portal. This site provides access to our information security management system (ISMS) documentation, including policies, procedures, and guides.

## Policies

<ul>
{% for policy in site.pages %}
  {% if policy.path contains 'Policies/' %}
  <li>
    <a href="{{ policy.url | relative_url }}">
      <strong>{{ policy.title }}</strong>
      <br>
      <small>{{ policy.path | split: '/' | last }}</small>
    </a>
  </li>
  {% endif %}
{% endfor %}
</ul>

## Procedures

<ul>
{% for procedure in site.pages %}
  {% if procedure.path contains 'Procedures/' %}
  <li>
    <a href="{{ procedure.url | relative_url }}">
      <strong>{{ procedure.title }}</strong>
      <br>
      <small>{{ procedure.path | split: '/' | last }}</small>
    </a>
  </li>
  {% endif %}
{% endfor %}
</ul>

## Guides

<ul>
{% for guide in site.pages %}
  {% if guide.path contains 'Guides/' %}
  <li>
    <a href="{{ guide.url | relative_url }}">
      <strong>{{ guide.title }}</strong>
      <br>
      <small>{{ guide.path | split: '/' | last }}</small>
    </a>
  </li>
  {% endif %}
{% endfor %}
</ul>

</div> 