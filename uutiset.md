---
layout: page
title: Uutiset
permalink: /uutiset/
---

<div class="section group">
  <div class="col span_1_of_2">
      <h2>Pääuutiset</h2>
      {% assign main_category_posts = site.categories[site.main_category] %}
      {%
        include functions/post-list.html
        posts=main_category_posts
        category_links=true
      %}
  </div>

  <div class="col span_1_of_2">
      <h2>Muut uutiset</h2>
      {%
        include functions/post-list.html
        posts=site.posts
        category_links=true
        exclude_category=site.main_category
      %}
  </div>
</div>
