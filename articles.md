---
layout: my-page
title: Articles
permalink: /articles/
---

<div class="posts">
  {% for post in site.categories.articles %}
    <article class="post">
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="button button-primary">Read More</a>
    </article>
  {% endfor %}
</div>
  


