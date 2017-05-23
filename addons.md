## Список аддонов

{% for addon in site.addons %}
- [{{ addon.name }}]({{ '/addons/' | append: addon.name | relative_url }}){% endfor %}
