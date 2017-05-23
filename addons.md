## Список аддонов

{% comment %}
  FIXME: hack! rewrite once Jekyll starts using Liquid 4
{% endcomment %}

{% capture addons %}
  {% for addon in site.addons %}|{{ addon.name | downcase }}#{{ addon.name }}{% endfor %}
{% endcapture %}

{% assign addons = addons | remove_first: '|' | split: '|' | sort %}

{% for addon in addons %}
  {% assign name = addon | split: '#' | last %}- [{{ name }}]({{ '/addons/' | append: name | relative_url }}){% endfor %}
