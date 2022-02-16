---
title: "AIPP - Scholarship"
layout: gridlay
excerpt: "AIPP scholarship"
sitemap: false
permalink: /scholarship/
---


# Scholarship

## Recent Work

AIPP meets weekly throughout the year to workshop scholarship at various stages of development. We highlight some of our recent, publically-available work below.
<br><br>

{% assign number_printed = 0 %}
{% for publi in site.data.highlights %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>

  {% if publi.award %}
  <p style="margin-top: 10px; background-color: #006699; color: #FFFFFF;text-align: center"><b>{{publi.award}}</b></p>
  {% endif %}
  {% if publi.image %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  {% endif %}
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Complete List

<!--there has to be a way to factor this nicely, but don't know
  enough of liquid syntax to do that right now-->

### 2022
  
{% for publi in site.data.publist2022 %}
  <hr class="rounded">
  <b>{{ publi.title }}</b> <br />
  <p style="color: #006699"><b>{{publi.award}}</b></p>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  <br>
{% endfor %}

<br>

### 2021
  
{% for publi in site.data.publist2021 %}
  <hr class="rounded">
  <b>{{ publi.title }}</b> <br />
  <p style="color: #006699"><b>{{publi.award}}</b></p>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  <br>
{% endfor %}

<br>

<!--
### 2020
  

{% for publi in site.data.publist2020 %}
  <hr class="rounded">
  <b>{{ publi.title }}</b> <br />
  <p style="color: #006699"><b>{{publi.award}}</b></p>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  <br>
{% endfor %}

<br>
-->
