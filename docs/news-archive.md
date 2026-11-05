---
layout: default
title: Архив новостей
parent: Главная
nav_order: 1
---

## Архив новостей

{% assign all_news = site.news | sort: "date" | reverse %}
{% assign news_by_season = all_news | group_by: "season" %}

{% for season in news_by_season %}
### {{ season.name }} учебный год

<div class="news-list">
  {% for news in season.items %}
    {% include news-card.html news=news %}
  {% endfor %}
</div>
{% endfor %}
