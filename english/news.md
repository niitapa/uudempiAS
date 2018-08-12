---
layout: page
title: News
subtitle: Newest
permalink: /news/
---

{% include functions/archive-navi.html %}

<div class="section group">
  <div class="col span_1_of_2">
      <h2>Main news</h2>
      {% assign main_category_posts = site.categories[site.main_category] %}
      {%
        include functions/post-list_en.html
        posts=main_category_posts
        category_links=true
      %}
  </div>

  <div class="col span_1_of_2">
      <h2>Other news</h2>
      {%
        include functions/post-list_en.html
        posts=site.posts
        category_links=true
        exclude_category=site.main_category
      %}
  </div>
</div>
