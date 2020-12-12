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
  <pubtit><a href="{{ publi.url }}">{{ publi.title }}</a>
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  </pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong>{{ publi.display }}</strong></p>
  <p class="text-danger"><strong> {{ publi.news }}</strong></p>
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

  {{ publi.title }} 
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## Wireless
{% for publi in site.data.publist %}

{% if publi.category1 == 1  or publi.category2 == 1%}

  {{ publi.title }} 
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## Robotics
{% for publi in site.data.publist %}

{% if publi.category1 == 2 or publi.category2 == 2%}

  {{ publi.title }} 
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## RFID Sensing and WISP
{% for publi in site.data.publist %}

{% if publi.category1 == 3  or publi.category2 == 3%}

  {{ publi.title }} 
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}

## Security and Misc.
{% for publi in site.data.publist %}

{% if publi.category1 == 4  or publi.category2 == 4%}

  {{ publi.title }} 
  {% if publi.pdf != 0 %}
  <strong><a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[pdf]</a></strong>
  {% endif %}
  <br />
  <em>{{ publi.authors }} </em><br />{{ publi.display }}

{% endif %}
{% endfor %}