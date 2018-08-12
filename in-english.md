---
layout: hallitus
title: In English
data: hallitus_en
placeholder_img: static/toimijat/aebaej_placeholder.png
---
<div class="home">
    
<article class="post">

  <div class="post-content">
    <div class="section group">

    <div class="col span_1_of_2">
      <div class="info_section">
        <h1 class="info_section__title">Important news</h1>
        {% assign main_category_posts = site.categories[site.main_category] %}
        {%
          include functions/post-list_en.html
          posts=main_category_posts
          limit=5
        %}
        <a href="News">All news</a>
      </div>
    </div>

    <div class="col span_1_of_2">
        <div class="info_section">
          <h1 class="info_section__title">What is AS?</h1>
          {% capture index_content %}{% include index_content_en.md %}{% endcapture %}
          {{ index_content | markdownify }}
        </div>

        <div class="info_section">
          <h1 class="info_section__title">Incoming events</h1>
          <ul id="event-list" class="event_list">
          </ul>
          <ul id="event-list-2" class="event_list">
          </ul>

          <a href="{{ "/events.html" | absolute_url }}">
            All events
          </a>
        </div>
    </div>

    </div>
  </div>

  <div class="section group">
    <div class="col span_2_of_2">
      <!-- SnapWidget -->
      <script src="https://snapwidget.com/js/snapwidget.js"></script>
      <iframe src="https://snapwidget.com/embed/477716" class="snapwidget-widget" allowTransparency="true" frameborder="0" scrolling="no" style="border:none; overflow:hidden; width:100%; "></iframe>
    </div>
  </div>

</article>

</div>