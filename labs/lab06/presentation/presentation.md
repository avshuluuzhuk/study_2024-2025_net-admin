---
## Front matter
lang: ru-RU
title: Статическая маршрутизация VLAN
subtitle: Лабораторная работа № 6
author:
  - Шулуужук А. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 12 февраль 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

## Цели и задачи

Настроить статическую маршрутизацию VLAN в сети.

# Выполнение лабораторной работы

## Выполнение лабораторной работы

![изменение топологии сети](image/1.png){#fig:001 width=40%}

## Выполнение лабораторной работы

![первоначальная настройка маршрутизатора](image/2.png){#fig:002 width=40%}

## Выполнение лабораторной работы

![настройка порта 24 коммутатора msk-donskaya-sw-1 как trunk-порт](image/3.png){#fig:003 width=40%}

## Выполнение лабораторной работы

![конфигурация VLAN-интерфейсов маршрутизатора](image/4.png){#fig:004 width=40%}

## Выполнение лабораторной работы

![проверка доступности оконечных устройств из разных VLAN](image/5.png){#fig:005 width=40%}

## Выполнение лабораторной работы

![режим симуляции, изучение содержимого передаваемого пакета](image/6.png){#fig:006 width=40%}

# Выводы

## Результаты работы

В результате выполнения лабораторной работы была проведена настройка статической маршрутизации VLAN в сети.
