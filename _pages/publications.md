---
title: 'Dickson Lab Publications'
layout: gridlay
excerpt: 'Dickson Lab -- Publications.'
sitemap: false
permalink: /publications/
---

# Publications

## Group highlights

For a full list of patents see [below](#patents) or go to [Google Scholar](https://scholar.google.com/citations?hl=en&user=p8fJn9EAAAAJ) for a completegit list of publications.

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

## Patents

<em>RM Dickson, TH Huang</em><br />Methods for Rapid Determinations of Antibiotic Susceptibility Phenotypes<br /><a href="https://patentimages.storage.googleapis.com/6b/1a/61/8fac2dc27ff01a/US20190338334A1.pdf"> US Patent App. 16/477,260 </a>

<em>RM Dickson, J Zheng</em><br /> Nano-sized optical fluorescence labels and uses thereof<br /> <a href="https://patentimages.storage.googleapis.com/0a/70/60/1edc3fabd0bf60/US7611907.pdf">US Patent 7,611,907</a>

<em>RM Dickson, J Zheng, LA Capadona, JT Petty, SA Patel, M Weck</em><br />Raman-Enhancing, and Non-Linear Optically Active Nano-Sized Optical Labels and Uses Thereof<br /> <a href="https://patentimages.storage.googleapis.com/2b/98/85/e8d982d4962e26/US20080118912A1.pdf">US Patent App. 10/598,722</a>

<em>RM Dickson, LA Lyon</em><br />Apparatus and method of optical transfer and control in plasmon supporting metal nanostructures<br /> <a href="https://patentimages.storage.googleapis.com/b3/2a/70/5aeb0f686883ac/US6539156.pdf">US Patent 6,539,156 </a>

<em>RY Tsien, R Heim, AB Cubitt, RM Dickson, WE Moerner</em><br />Photochromic fluorescent proteins and optical memory storage devices based on fluorescent proteins<br /> <a href="https://patentimages.storage.googleapis.com/f4/9f/78/92851c52c57849/US6046925.pdf">US Patent 6,046,925</a>

<em></em>

## A longer list of publications

{% for publi in site.data.publist %}

{{ publi.title }} <br />
<em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
