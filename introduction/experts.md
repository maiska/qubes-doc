---
lang: en
layout: experts
permalink: /experts/
ref: 119
title: Experts
---

{% if page.lang == nil or page.lang == "en" %}
        {% assign experts = site.data.experts %}
{% else %}
        {% assign experts = site.data.translation[page.lang].experts %}
        {% if experts == nil or experts.size == 0 %}
                {% assign experts = site.data.experts %}
        {% endif %}
{% endif %}
{% assign experts = experts | where_exp: "item", "item.experts == nil" | first %}

<div class="home-content container">
  <div class="row more-top">
    <div class="col-lg-12 col-md-12">
      <h2 class="text-center"><i class="fa fa-quote-left"></i> {{ experts.title }}</h2>
    </div>
  </div>
  <div class="white-box more-bottom">

{% for item in experts.expert %}

    <div class="row featured-quotes">
      <div class="col-lg-3 col-md-3 text-center">
        <a class="avatar-large" href="{{ item.avatar}}" target="_blank">
          <img src="{{ item.img }}">
        </a>
      </div>
      <div class="col-lg-9 col-md-9 more-top">
        <a href="{{ item.tweet }}" target="_blank">
          <blockquote>"{{ item.quote }}"
            <i class="fa fa-twitter fa-fw" aria-hidden="true"></i>
            <footer>{{ item.name }}<cite>, {{ item.occupation }}</cite></footer>
          </blockquote>
        </a>
      </div>
    </div>

{% endfor %}
  </div>
  {% include footer.html %}
</div>
