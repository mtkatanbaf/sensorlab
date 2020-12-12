---
title: "Sensor Systems Lab - Publications"
layout: gridlay
excerpt: "Sensor Systems Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

(For a full list see [Recent Publications](#recent=publications), [Wireless](#wireless), [Robotics](#robotics), [RFID Sensing and WISP](#rfid-sensing-and-wisp), [Security and Misc.](#security-and-misc.)  )

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit><a href="{{ publi.url }}">{{ publi.title }}</a></pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong>{{ publi.display }}</strong></p>
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


## Recent Publications

{% for publi in site.data.publist %}

{% if publi.year > 2016 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## Wireless
{% for publi in site.data.publist %}

{% if publi.category == 1 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## Robotics
{% for publi in site.data.publist %}

{% if publi.category == 2 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## RFID Sensing and WISP


## Security and Misc.