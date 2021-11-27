---
## Front matter
title: "Лабораторная работа №6: Мандатное
разграничение прав в Linux"
subtitle: "*дисциплина: Информационная безопасность*"
author: "Швец Сергей Сергеевич"
date: 2021, 27 november

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true

---


# Цель работы

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1
.
Проверить работу SELinx на практике совместно с веб-сервером
Apache.

# Выполнение работы

## Установка httpd

Установка httpd

![httpd](1.jpg){ #fig:001 width=70% }

## Вход в систему

Войдите в систему с полученными учётными данными и убедитесь, что
SELinux работает в режиме enforcing политики targeted с помощью команд getenforce и sestatus.

![Guest](2.jpg){ #fig:002 width=70% }

## Обращение

Обращение с помощью браузера к веб-серверу, запущенному на
компьютере

![обращение к веб-серверу](3.jpg){ #fig:003 width=70% }


## Контекст


Определение контекста безопасности .

![контекст безопасности ](4.jpg){ #fig:005 width=70% }

## Состояние

Текущее состояние переключателей SELinux для Apache.

![просмотр состояния](7.jpg){ #fig:006 width=70% }

## Файлы и поддиректории

Определение типа файлов и поддиректорий, находящихся в директории.

![Расширинные атрибуты](9.jpg){ #fig:008 width=70% }

## test.html

Создание файла test.html

![test.html](6.jpg){ #fig:007 width=70% }

## Учетная запись

Создание в домашней директории поддиректорию dir1 командой mkdir dir1. Определение командами ls -l и lsattr прав доступа и расширенных атрибутов.

![Поддиректория](8.jpg){ #fig:009 width=70% }


## Учетная запись

Снятие с директории dir1 всех атрибутов командой chmod 000 dir1.

![Снятие атрибутов](9.jpg){ #fig:011 width=70% }

## log-файл

Просмотр системного log-файла.

![Создание файла](10.jpg){ #fig:012 width=70% }

## Попытка перезапуска

Попытка перезапуска сервера.

![17](11.jpg){ #fig:013 width=70% }

## log-файлы

tail -nl /var/log/messages.

![18](13.jpg){ #fig:013 width=70% }

## Список портов

semanage port -l | grep http_port_t.

![19](12.jpg){ #fig:013 width=70% }

# Выводы

Я ознакомился с базовыми с технологией SELinux. Развил навыки одминистратора и проверил работу SELinux на практике.
