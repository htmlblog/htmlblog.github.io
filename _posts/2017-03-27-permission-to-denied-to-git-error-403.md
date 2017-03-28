---
title: 'Git ошибка remote: Permission to user/repo denied to user/other-repo'
date: 2017-03-27 07:03:00 Z
permalink: "/permission-to-denied-to-git-error-403"
categories:
- useful
tags:
- git
- github
description: 'Варианты решения ошибки Git remote: Permission to denied to fatal: unable
  to access The requested URL returned error: 403.'
header: 'Решение ошибки remote: Permission to user/repo denied to user/other-repo.
  fatal: unable to access user/repo: The requested URL returned error: 403'
layout: post
---

В данном уроке рассмотрим варианты решения данной оишбки:

> **remote: Permission to user/repo denied to user/other-repo.**
> **fatal: unable to access user/repo: The requested URL returned error: 403** 

Возникает она чаще всего у новичков при попытке сделать **$ git push**. 
Пример на скриншоте ниже.

![git-permission-to-denied-to-error-403.jpg](/uploads/git-permission-to-denied-to-error-403.jpg)

Данная ошибка возникает довольно часто при работе с Git в терминале Windows. Суть ошибка довольно таки простая, но почему-то в интернете постоянно создаются темы с вопросом на данную тему и нет внятного ответа на русском языке.

Ошибка говорит нам о том, что мы пытаемся отправить данные в чужой репозиторий. И о том, что текущий пользователь Git не имеет прав для отправки данных в указанный в команде репозиторий.

<hr>

### Существует два способа решить данную ошибку:

**1. Дать текущему пользователю права для работы с репозиторием**

Данный способ подойдет, если вы являетесь владельцем обоих учетных записей указанных в ошибке. 