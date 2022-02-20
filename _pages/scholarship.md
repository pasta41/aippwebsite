---
title: "AIPP - Scholarship"
layout: gridlay
excerpt: "AIPP scholarship"
sitemap: false
permalink: /scholarship/
---


# Scholarship

## Recently Workshopped Pieces

AIPP meets weekly throughout the year to workshop scholarship at various stages of development. We highlight below some of this recent work that has been made publically available.

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


## Full List

{% for publi in site.data.publist %}
  <hr class="rounded">
  <b>{{ publi.title }}</b> <br />
  <p style="color: #006699"><b>{{publi.award}}</b></p>
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
  <br>
{% endfor %}
<br>
