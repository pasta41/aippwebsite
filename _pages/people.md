---
title: "AIPP - People"
layout: gridlay
excerpt: "AIPP group members"
sitemap: false
permalink: /people/
---

# People

{% for member in site.data.people %}

<div class="col-sm-6 clearfix" style="padding-bottom:50px">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  {% if member.website %}
  <h4><a href="{{member.website}}">{{member.name}}</a></h4>
  {% else %}
  <h4>{{member.name}}</h4>
  {% endif %}
  
  <h5>{{ member.title }}</h5>
  <h6>{{ member.info }}</h6>
  <br>
</div>
<div class="col-sm-6 clearfix" style="padding-bottom:50px">
{{member.about}}
<br><br><br><br>
</div>
<hr class="rounded">
<br><br>


<!--Do we want to do an "Alumni" list?-->

{% endfor %}
<br><br><br><br><br>