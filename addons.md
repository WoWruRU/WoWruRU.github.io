## Установка аддонов
1. Скачать нужный Вам аддон
2. Распаковать Zip-файл
3. [опционально] Если в названии папки с аддоном есть приписка "-master", то ее необходимо удалить. Например название папки "Caterer-master", следовательно необходимо переименовать ее в "Caterer"
4. Скопировать папку с аддоном в Директорию-Wow\Interface\AddOns\
5. Перезапустить WoW

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
