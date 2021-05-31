---
name: Marybeth Arcodia
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Marybeth Arcodia</h2>
    <p><img src="{{ site.url }}/assets/img/Arcodia_headshot.png" alt="Marybeth Arcodia headshot" width="40%" align="left" hspace="30">Marybeth Arcodia is an Atmospheric Science Ph.D. Candidate with Dr. Ben Kirtman studying climate variability and dynamics. Her research looks at how particular atmospheric and oceanic conditions in the tropical Indian and Pacific Oceans impact regional weather patterns and extreme events in the United States on subseasonal (two week to two month) time scales. Using a combination of climate models and observations, she analyzes the interference from the MJO and ENSO wave signals to better understand the mechanisms and variability of tropical-extratropical teleconnection patterns. She received her BA in Mathematics from Georgetown University in 2014. Outside of research, she enjoys running, paddle boarding, and tacos. </p>
    <a href="https://twitter.com/mbarcodia" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a><br><br><br>
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

