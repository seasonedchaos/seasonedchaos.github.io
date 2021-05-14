---
name: Kelsey Malloy
layout: main
---

<div class="author-bio">
  Check back later for bio.
</div>

<div class="post-list">
  <h2>Posts by {{ page.name }}:</h2>
  {% for post in site.posts %}
    {% assign authorCount = page.authors | size %}
    {% for author in post.authors %}
      {% if author == page.name %}
        <div class="author-list">
          <span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
          <small><span>| {{ post.date | date_to_string }}</span></small>
        </div>
      {% endif %}
    {% endfor %}
  {% endfor %}
</div>
