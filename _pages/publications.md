---
title: "AIPP - Publications"
layout: gridlay
excerpt: "AIPP publications"
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

<!-- finish code for de-coupling awards from highlighting-->

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>

  {% if publi.highlight == 1 %}
  <p style="margin-top: 10px; background-color: #006699; color: #FFFFFF;text-align: center"><b>{{publi.award}}</b></p>
  {% endif %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
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
