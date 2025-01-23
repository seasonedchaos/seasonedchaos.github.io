---
name: Kayla Besong
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Kayla Besong</h2>
    <p><img src="{{ site.url }}/assets/img/Besong_headshot.jpeg" alt="Kayla Besong headshot" width="30%" align="left" hspace="30">I am currently a Duty Scientist at the Pacific Tsunami Warning Center in Honolulu, HI where we are on watch 24/7 responding to and preparing for tsunami events. I have taken great interest in the RIFT forecast model, improving operational procedures, and product dissemination. Previously I worked as an air quality data scientist at Sonoma Technology Inc., supporting a variety of environmental consulting projects mostly related to wildfires and air quality. My Ph.D. was completed in December 2022 from the University of Miami Rosenstiel School, where my work focused on atmospheric blocking, analysis techniques associated with them, how they relate to the North Atlantic Oscillation, and how well that relationship is represented in a global climate model. I also possess a BA in environmental resources engineering from the SUNY College of Environmental Science and Forestry in Syracuse, NY. When I am not working you can find me making nachos, pasta, or other kitchen concoctions, helping out with the sea turtles on the North Shore of O’ahu, or cheering for a Pittsburgh sports team.</p>
    <a href="https://bsky.app/profile/drkaylabesong.bsky.social" target="_blank">BlueSky</a> | <a href="https://www.linkedin.com/in/kayla-besong-613a6110b/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a><br><br><br><br><br><br><br><br><br><br><br>
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

