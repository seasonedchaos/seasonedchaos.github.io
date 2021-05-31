---
name: Kurt Hansen
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Kurt Hansen</h2>
    <p><img src="{{ site.url }}/assets/img/Hansen_headshot.jpg" alt="Kurt Hansen headshot" width="30%" align="left" hspace="30">I am a 5th year Ph.D student at the University of Miami RSMAS under Sharan Majumdar and Ben Kirtman. My research focuses on subseasonal variability of Atlantic hurricane activity. I received my Bachelors in atmospheric science at the University of Albany. In my free time I like rock climbing, kayaking, and long romantic unicycle rides by the beach. </p>
    <a href="https://twitter.com/all4hurricanes1" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a><br><br><br><br><br>
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
  </div> <!-- End Page Content -->
</article> <!-- End Article Page -->
