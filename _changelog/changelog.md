## История изменений

{% assign changelog = site.changelog | reverse %}
{% for change in changelog %}
- [{{ change.date | date: "%d.%m.%Y" }}]({{ change.url }}){% endfor %}
