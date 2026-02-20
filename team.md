---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---
<h1>Team</h1>
<center><img src="/images/team.jpg" style="border-radius: 0;" width="1200" height="250" align="center"></center>
<br>

{% assign number_printed = 0 %}
{% for member in site.data.team_faculty %}

{% assign even_odd = number_printed | modulo: 3 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="float:left; width:30%; margin-right:8px;" />
  
  <div style="overflow:hidden;">
  <h4>{{ member.name }}</h4>
  <h5><i>{{ member.info }}</i></h5>
  {{ member.email }}
  <br>{{ member.web }}
  <br>{{ member.since }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 3 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% if even_odd == 2 %}
</div>
{% endif %}

<br><br>
