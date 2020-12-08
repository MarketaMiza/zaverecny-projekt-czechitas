---
layout: layouts/moje-sablona
nadpis: Report
menu: report
---

<div class="article-main"> 
<section class="article-box">
{% for clanek in collections.clanky %}
<article class="article-preview">
<a href="{{ clanek.url }}">
<h3> {{ clanek.data.nadpis }} </h3>
</a>
<div class="imageholder">
<img class="article-preview__image"
 src="/images/{{ clanek.data.image }}" alt="{{ clanek.data.nadpis }}">
</div>
<p> {{ clanek.data.perex | truncate(150, true, "...") }} </p>
<p>
  <a href="{{ clanek.url }}">
    <button class="button-link">číst dál</button>
  </a>
</p>
</article>
{% endfor %}
</section>
</div>


