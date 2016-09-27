---
title: Storie
permalink: "/storie/"
layout: page
---

{% assign storie = (site.storie | sort: 'date') %}

<div class="posts">
  {% for post in storie reversed%}
      <article class="post">
        <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

        <div class="entry">
          {{ post.excerpt }}
        </div>

        <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Leggi tutto</a>
      </article>
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>
  {% endfor %}
</div>
