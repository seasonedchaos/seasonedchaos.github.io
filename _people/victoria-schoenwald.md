---
name: Victoria Schoenwald
layout: main
---

<article class="article-page">
  <div class="page-content">
    <h2>Victoria Schoenwald</h2>
    <p><img src="{{ site.url }}/assets/img/Schoenwald_headshot.jpg" alt="Victoria Schoenwald headshot" width="40%" align="left" hspace="30">I am a 4th year atmospheric science Ph.D. student interested in coastal flooding predictability and sea level rise. My current project is studying how large-scale climate patterns and ocean circulation affect sea level variability on the East Coast of the United States. I earned a bachelor’s degree in biology from Sacred Heart University in Fairfield, CT where I worked on coastal restoration and groundwater research projects. Outside of science, I really enjoy hiking, travelling and gardening.  </p>
    <a href="https://twitter.com/vkschoenwald" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a> | <a href="https://www.linkedin.com/in/victoria-schoenwald-69346a13b/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a><br><br><br><br><br><br><br><br><br><br><br>
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
