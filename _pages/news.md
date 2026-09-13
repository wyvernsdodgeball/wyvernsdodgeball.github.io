---
layout: default
title: "News"
description: "Tutte le ultime notizie dai Wyverns Dodgeball – risultati, eventi, aggiornamenti dal mondo del dodgeball a Roma."
keywords: "news dodgeball roma, risultati wyverns dodgeball, eventi dodgeball roma"
permalink: /news/
---

<section class="section-news">
  <div class="container">
    <div class="section-header" data-reveal>
      <span class="section-tag">Aggiornamenti</span>
      <h2>NEWS &<br>RISULTATI</h2>
      <div class="divider"></div>
      <p>Tutto quello che succede in casa Wyverns.</p>
    </div>

    <div class="news-grid" data-reveal>
      {% for post in site.posts %}
      <article class="news-card">
        {% if post.image %}
        <div class="news-card-image">
          <img src="{{ site.baseurl }}{{ post.image }}" alt="{{ post.title }}" loading="lazy">
        </div>
        {% endif %}
        <div class="news-card-body">
          {% if post.category %}<span class="section-tag">{{ post.category }}</span>{% endif %}
          <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
          <time datetime="{{ post.date | date: '%Y-%m-%d' }}">{{ post.date | date: "%d %B %Y" }}</time>
          {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>{% endif %}
          <a href="{{ site.baseurl }}{{ post.url }}" class="news-read-more">Leggi →</a>
        </div>
      </article>
      {% endfor %}

      {% if site.posts.size == 0 %}
      <div class="news-empty">
        <p>Le prime news arrivano presto. Seguici su <a href="{{ site.social.instagram }}" target="_blank" rel="noopener">Instagram</a> per restare aggiornato!</p>
      </div>
      {% endif %}
    </div>
  </div>
</section>
