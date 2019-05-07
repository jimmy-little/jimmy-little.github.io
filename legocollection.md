---

layout: page
title: 2018 Lego Advent Calendar
date: 2018-03-17
excerpt: Check out my 2018 Lego Advent Calendar Series. Originally posted on Instagram, but available here for posterity.
img: legoadvent.png
tn: legoadvent.png
tags: [Lego, Star Wars]

---

{% for lego-advent in site.lego-advent %}

<article class="article-page-social">
<div class="wrap-content">
<div class="page-content">
<div class="social">
{% if lego-advent.img %}
      <img class="social-img" src="{{ site.url }}/assets/img/post/{{ lego-advent.img }}" alt="{{ lego-advent.title }}">
{% endif%} 
{{ lego-advent.excerpt }}
<span class="tag-social">Originally posted on <a href="{{ lego-advent.link }}"><i class="fa fa-instagram"></i> {{ lego-advent.via }}</a> on {{ lego-advent.date | date: '%b %d, %Y'}}</span>
</div>
    </div> <!-- End Wrap Content -->
  </div> <!-- End Page Content -->
</article> <!-- End Article Page -->

{% endfor %}  