---
title: "Relax ML Lab - News"
layout: textlay
excerpt: "Relax ML Lab at Cornell University"
sitemap: false
permalink: /allnews.html
---

# News

<ul>
{% for article in site.data.news %}
<li> <p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
</li>
{% endfor %}
</ul>
<br>
<br>
