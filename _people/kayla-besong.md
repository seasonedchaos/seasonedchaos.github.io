---
name: Kayla Besong
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Kayla Besong</h2>
    <p><img src="{{ site.url }}/assets/img/Besong_headshot.png" alt="Kayla Besong headshot" width="40%" align="left" hspace="30">I am a soon to be 5th year PhD candidate who studies atmospheric blocking, how the location of blocking events affect U.S. weather, and influences on the blocking lifecycle from the ocean and atmosphere. Other work interests include the intersection of climate change and sustainability, effective science communication, and python programming. My undergraduate degree is a BA in environmental resources engineering from the SUNY College of Environmental Science and Forestry in Syracuse, NY. When I am not working you can find me making nachos or other kitchen concoctions, taking weather time-lapse videos, or really, anywhere outside.</p>
    <a href="https://twitter.com/kayla_beesting" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a> | <a href="https://www.linkedin.com/in/kayla-besong-613a6110b/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a><br><br><br><br><br><br><br><br><br><br><br>
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

