---
title: "Relax ML Lab - Team"
layout: gridlay
excerpt: "Relax ML Team members"
sitemap: false
permalink: /team/
---

# Team Lead

{% assign number_printed = 0 %}
{% for lead in site.data.leads %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-8 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ lead.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ lead.name }}</h4>
  <i>{{ lead.info }}<br></i>
  <ul style="overflow: hidden">

    <li><b>Email</b>: <{{ lead.email }}></li>
    <li><b>Website</b>: <a href="{{ lead.website}}">{{ lead.website}}</a></li>

  </ul>
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

# Group Members

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>
  <ul style="overflow: hidden">

    <li><b>Email</b>: <{{ member.email }}></li>
    <li><b>Website</b>: <a href="{{ member.website}}">{{ member.website}}</a></li>
    <li><b>Research area</b>: {{member.research}}</li>

  </ul>
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
