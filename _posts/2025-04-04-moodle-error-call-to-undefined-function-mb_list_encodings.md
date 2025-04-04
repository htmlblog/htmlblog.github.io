---
title: 'Ошибка Moodle: Call to undefined function mb_list_encodings()'
date: 2025-04-04 02:03:00 Z
categories:
- useful
tags:
- moodle
- php
- mbstring
description: 'Варианты исправления ошибки Moodle: Call to undefined function mb_list_encodings(). Чаще всего ошибка возникает при обновлении Moodle или PHP.'
header: 'Исправление ошибки Moodle: Call to undefined function mb_list_encodings()'
layout: post
thumb: "/uploads/moodle-error-call-to-undefined-function-mb_list_encodings.jpg"
---

<p>Ошибка <b><code inline="">Call to undefined function mb_list_encodings()</code></b> в Moodle, как правило, связана с отсутствием расширения <code inline="">mbstring</code> для PHP, которое необходимое для работы с многоязычными строками.</p>
<p>Чтобы решить эту проблему, нужно убедиться, что на сервере установлено расширение <code inline="">mbstring</code> для PHP. Вот шаги, которые помогут это исправить:</p>
<h3>1. Установка расширения <code inline="">mbstring</code></h3>
<p>В зависимости от операционной системы, можно использовать следующие команды для установки расширения.</p>
<h4>Для Debian/Ubuntu:</h4>
<blockquote>
	<pre><code class="language-bash">sudo apt-get install php-mbstring
sudo systemctl restart apache2   # Если используется Apache
sudo systemctl restart php-fpm   # Если используется PHP-FPM
</code></pre>
</blockquote>
<h4>Для CentOS/RHEL:</h4>
<blockquote>
	<pre><code class="language-bash">sudo yum install php-mbstring
sudo systemctl restart httpd     # Если используется Apache
sudo systemctl restart php-fpm   # Если используется PHP-FPM
</code></pre>
</blockquote>
<h4>Для Windows:</h4>
<p>Если вы используете PHP на Windows, вам нужно включить расширение <code inline="">mbstring</code> в конфигурационном файле <code inline="">php.ini</code>. Найдите строку:</p>
<blockquote>
	<pre><code class="language-ini">;extension=mbstring
</code></pre>
</blockquote>
<p>И удалите точку с запятой (<code inline="">;</code>), чтобы строка выглядела так:</p>
<blockquote>
	<pre><code class="language-ini">extension=mbstring
</code></pre>
</blockquote>
<p>После этого перезапустите ваш сервер.</p>
<h3>2. Проверка установки</h3>
<p>После установки расширения <code inline="">mbstring</code>, можно проверить, что оно активировано, с помощью следующей команды:</p>
<blockquote>
	<pre><code class="language-bash">php -m | grep mbstring
</code></pre>
</blockquote>
<p>Если <code inline="">mbstring</code> появляется в списке, значит, оно успешно установлено и активировано.</p>
<h3>3. Перезапуск веб-сервера</h3>
<p>После установки или активации расширения, не забудьте перезапустить веб-сервер (например, Apache или PHP-FPM), чтобы изменения вступили в силу.</p>
<p>Если после этого проблема не исчезла, дайте знать, и мы попробуем другие варианты!</p>
