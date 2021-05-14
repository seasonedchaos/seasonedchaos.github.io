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
      <span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
        <small><span>| {{ post.date | date_to_string }}</span></small>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>

