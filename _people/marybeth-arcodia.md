---
name: Marybeth Arcodia
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Marybeth Arcodia</h2>
    <p><img src="{{ site.url }}/assets/img/Arcodia_headshot.png" alt="Marybeth Arcodia headshot" width="40%" align="right" hspace="30">Marybeth Arcodia received her Ph.D. in Atmospheric Science from the University of Miami's Rosenstiel School of Marine and Atmospheric Science in 2021. She was advised by Dr. Ben Kirtman and studied climate variability and dynamics. She is currently working as a Research Scientist I at Colorado State University using explainable artificial intelligence techniques to better understand climate predictability from subseasonal-to-decadal timescales (S2D) and climate change signals. She received her BA in Mathematics from Georgetown University in 2014. Outside of research, she enjoys running, paddle boarding, long walks on the beach, and ice cream. </p>
    <a href="https://twitter.com/mbarcodia" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a> | <a href="https://marybetharcodia.wixsite.com/earth" target="_blank">my personal website</a><br><br><br><br><br><br><br><br><br><br><br>
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

