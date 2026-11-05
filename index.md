---
layout: default
title: Главная
nav_order: 1
has_children: true
permalink: /
---

## Олимпиада по физике им. Дж. Кл. Максвелла
{: .page-title }

Олимпиада им. Дж. Кл. Максвелла проводится для учеников 7–8 классов в качестве замены регионального и заключительного этапов Всероссийской олимпиады школьников по физике.

{% assign home_news = site.news | where: "home", true | sort: "date" | reverse %}

<div class="news-list">
{% for news in home_news %}
  {% include news-card.html news=news %}
{% endfor %}
</div>
