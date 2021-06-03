---
name: Kelsey Malloy
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Kelsey Malloy</h2>
    <p><img src="{{ site.url }}/assets/img/Malloy_headshot.jpg" alt="Kelsey Malloy headshot" width="40%" align="right" hspace="30">I am a 4th year PhD candidate interested in climate variability, climate dynamics, and predictability. I received my B.S. in Atmospheric and Oceanic Science from Univ. of Maryland in 2017. My current research is on the predictability of U.S. summer hydroclimate through understanding large-scale remote influences (AKA, teleconnections) on the Great Plains low-level jet. I'm also interested in science communication, outreach, and general data science topics. In my free time, you can often find me doing yoga, reading, or spending time outdoors. </p>
    <a href="https://twitter.com/kelseyl4tely" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a> | <a href="https://www.linkedin.com/in/kelsey-malloy-5a2551149/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a> | <a href="https://kelseymalloy.github.io/" target="_blank">my personal website</a><br><br><br><br><br><br><br><br><br><br><br>
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
