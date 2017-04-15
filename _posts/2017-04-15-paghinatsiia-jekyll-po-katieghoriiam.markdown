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

```
<!-- Pagination links -->
  {% if paginator.total_pages > 1 %}
	<div class="pagination">
	  {% if paginator.previous_page == 1 %}
		<a href="{{ '/news/' | prepend: site.baseurl | replace: '//', '/' }}" class="page-item">&laquo;</a>
	  {% elsif paginator.previous_page%}
		<a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}" class="page-item">&laquo;</a>
	  {% else %}
		<span class="page-item">&laquo;</span>
	  {% endif %}
	
	  {% for page in (1..paginator.total_pages) %}
		{% if page == paginator.page %}
		  <span class="page-item">{{ page }}</span>
		{% elsif page == 1 %}
		  <a href="{{ '/news/' | prepend: site.baseurl | replace: '//', '/' }}" class="page-item">{{ page }}</a>
		{% else %}
			<!--  сделать ссылку формата localhost:4000/test/page2/ -->
		  <a href="{{ site.paginate_path | prepend: site.baseurl | replace: '//', '/news/' | replace: ':num', page }}" class="page-item">{{ page }}</a>
		{% endif %}
	  {% endfor %}
	
	  {% if paginator.next_page %}
		<a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}" class="page-item">&raquo;</a>
	  {% else %}
		<span class="page-item">&raquo;</span>
	  {% endif %}
	</div>
	{% endif %}
<!-- Pagination links End-->
```