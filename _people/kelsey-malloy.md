---
name: Kelsey Malloy
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Kelsey Malloy</h2>
    <p><img src="{{ site.url }}/assets/img/Malloy_headshot.jpg" alt="Kelsey Malloy headshot" width="40%" align="right" hspace="30">I am an Assistant Professor in Climatology at University of Delaware Dept. of Geography and Spatial Sciences interested in climate variability, climate dynamics, weather-climate interactions, and predictability. I received my Ph.D. in Atmospheric Sciences from University of Miami Rosenstiel School. I'm also interested in science communication, outreach, and general data science topics. In my free time, you can often find me doing puzzles, reading, or spending time outdoors. </p>
    <a href="https://twitter.com/kmmalloy" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a> | <a href="https://www.linkedin.com/in/kelsey-malloy-5a2551149/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a> | <a href="https://kelseymalloy.github.io/" target="_blank">my personal website</a><br><br><br><br><br><br><br><br><br><br><br>
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
