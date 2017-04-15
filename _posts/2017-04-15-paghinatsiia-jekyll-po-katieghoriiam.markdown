---
title: Пагинация постов Jekyll по категориям
date: 2017-04-15 11:30:00 Z
permalink: jekyll-post-pagination-in-category
categories:
- jekyll
header: 'Постраничный вывод постов в категориях Jekyll '
description: В данной статье рассмотрим как подключить плагин для постраничного вывода
  постов в категориях Jekyll. Пагинация постов Jekyll по категориям важный вопрос
  при создании блога.
layout: post
---

7
`<!-- Pagination links -->`
```xml
{% if paginator.total_pages > 1 %}
```
~~~xml
{% endif %}
~~~
`<!-- Pagination links End-->`