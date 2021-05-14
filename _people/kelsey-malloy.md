---
name: Kelsey Malloy
layout: main
---

Bio TBD


{% capture site_authors %}{% for author in site.authors %}{{ author | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign authors_list = site_authors | split:',' | sort %}

<h1>Posts</h1>
<!--cycles through tag list and creates subheader for each tag name...-->
{% for this_author in authors_list %}
<!--  lists all posts corresponding to specific tag...-->
  {% for post in site.authors[this_author] %}{% if post.title != null %}
  <div class="author-list">
      <span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
      <small><span>| {{ post.date | date_to_string }}</span></small>
  </div>
  {% endif %}{% endfor %}
{% endfor %}

