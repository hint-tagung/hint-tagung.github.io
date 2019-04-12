---
titel: Gäste
---


# Gäste
{% assign gaeste = site.gaeste | sort_natural: 'nachname' %}
{% for gast in gaeste  %}
<div class="media mt-3">
{% if gast.bild %}
<img src="/assets/img/gaeste/{{gast.bild}}" width="128" height="128" class="mr-3 img-thumbnail rounded" />
{% endif %}
<div class="media-body">
<h5 class="gastname mt-0">{{gast.vorname}} {{gast.nachname}}</h5>
{{gast.content}}
</div>
</div>
{%endfor %}
