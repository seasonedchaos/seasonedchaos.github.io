---
name: Kelsey Malloy
layout: main
---

Bio TBD
<br><br><br><br><br>

{% capture site_authors %}{% for author in site.authors %}{{ author | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign authors_list = site_authors | split:',' | sort %}

<h1>Posts</h1>
<!--cycles through tag list and creates subheader for each tag name...-->
{% for this_author in authors_list %}
<h2 id="{{ this_author | cgi_escape }}">{{ this_author }}</h2>
<!--  lists all posts corresponding to specific tag...-->
  {% for page in site.pages %}
  {% for post in page.authors[this_author] %}{% if post.title != null %}
  <div class="author-list">
      <span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></span>
      <small><span>| {{ post.date | date_to_string }}</span></small>
  </div>
  {% endif %}{% endfor %}
{% endfor %}

