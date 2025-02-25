---
layout: page
title: Debug Links
permalink: /debug/
---

# Site Configuration Information

- Site URL: {{ site.url }}
- Site BaseURL: {{ site.baseurl }}
- Full URL: {{ site.url }}{{ site.baseurl }}

# All Pages and Their URLs

<ul>
{% for page in site.pages %}
  <li>
    <strong>{{ page.title }}</strong> - 
    Path: {{ page.path }} - 
    URL: <a href="{{ page.url | relative_url }}">{{ page.url }}</a> - 
    Absolute URL: <a href="{{ site.url }}{{ site.baseurl }}{{ page.url }}">{{ site.url }}{{ site.baseurl }}{{ page.url }}</a> - 
    Permalink: {{ page.permalink }}
  </li>
{% endfor %}
</ul>

# Link Tests

- [Test relative_url filter]({{ "/test" | relative_url }})
- [Test absolute_url filter]({{ "/test" | absolute_url }})
- [Test direct link](/test)
- [Test with baseurl]({{ site.baseurl }}/test) 