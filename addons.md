## Список аддонов

{% for addon in site.addons %}
- [{{ addon.display_name | default: addon.name }}]({{ '/addons/' | append: addon.name | relative_url }}){% endfor %}
