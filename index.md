---
title: Инструкции, размещенные в сети
permalink: index.html
layout: home
---

# Каталог содержимого

Ниже приводятся ссылки на все задания и ролики.

## Задания

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Модуль | Задание |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Ролики

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" %}
| Модуль | Ролик |
| --- | --- | 
{% for activity in demos  %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
