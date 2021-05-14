---
name: Kelsey Malloy
layout: main
---

<h2>Posts by {{ page.name }}:</h2>
<ul>
{% for post in site.posts %}
  {% assign authorCount = page.authors | size %}
  {% for author in post.authors %}
    {% if author == page.name %}
      <div class="tag-list">
        <span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
        <small><span>| {{ post.date | date_to_string }}</span></small>
      </div>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>
