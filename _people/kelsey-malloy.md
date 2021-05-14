---
name: Kelsey Malloy
layout: main
---

Bio TBD
<br><br><br><br><br>

<h2>Posts by {{ page.name }}:</h2>
<ul>
{% for post in site.posts %}
  {% assign authorCount = page.authors | size %}
  {% for author in post.authors %}
    {% if author == page.name %}
      <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>

