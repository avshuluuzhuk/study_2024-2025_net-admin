---
## Front matter
title: "Статическая маршрутизация в Интернете. Настройка"
subtitle: "Лабораторная работа  № 14"
author: "Шулуужук Айраана НПИбд-02-22"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Настроить взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.
 
# Выполнение лабораторной работы

Настроим связь между территориями (рис. [-@fig:001]) (рис. [-@fig:002]) (рис. [-@fig:003]) (рис. [-@fig:004]) (рис. [-@fig:005])

![Настройка интерфейсов коммутатора provider-sw-1](image/1.png){#fig:001 width=70%}

![Настройка интерфейсов маршрутизатора msk-donskaya-gw-1](image/2.png){#fig:002 width=70%}

![Настройка интерфейсов маршрутизатора msk-q42-gw-1](image/3.png){#fig:003 width=70%}

![Настройка интерфейсов коммутатора sch-sochi-sw-1](image/4.png){#fig:004 width=70%}

![Настройка интерфейсов маршрутизатора sch-sochi-gw-1](image/5.png){#fig:005 width=70%}

Настроим оборудование, расположенное в квартале 42 в Москве (рис. [-@fig:006]) (рис. [-@fig:007]) (рис. [-@fig:008]) (рис. [-@fig:009])

![Настройка интерфейсов маршрутизатора msk-q42-gw-1](image/6.png){#fig:006 width=70%}

![Настройка интерфейсов коммутатора msk-q42-sw-1](image/7.png){#fig:007 width=70%}

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1](image/8.png){#fig:008 width=70%}

![Настройка интерфейсов коммутатора msk-hostel-sw-1](image/9.png){#fig:009 width=70%}

Настроим оборудование, расположенное в филиале в г. Сочи (рис. [-@fig:010]) (рис. [-@fig:011])

![Настройка интерфейсов маршрутизатора sch-sochi-gw-1](image/10.png){#fig:010 width=70%}

![Настройка интерфейсов коммутатора sch-sochi-sw-1](image/11.png){#fig:011 width=70%}

Настроим статическую маршрутизацию между территориями (рис. [-@fig:012]) (рис. [-@fig:013]) (рис. [-@fig:014])

![Настройка маршрутизатора msk-donskaya-gw-1](image/12.png){#fig:012 width=70%}

![Настройка маршрутизатора msk-q42-gw-1](image/13.png){#fig:013 width=70%}

![Настройка маршрутизатора sch-sochi-gw-1](image/14.png){#fig:014 width=70%}

Настроим статическую маршрутизацию на территории квартала 42 в г. Москве (рис. [-@fig:015]) (рис. [-@fig:016]) 

![Настройка маршрутизатора msk-q42-gw-1](image/15.png){#fig:015 width=70%}

![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1](image/16.png){#fig:016 width=70%}

Настроим NAT на маршрутизаторе msk-donskaya-gw-1 (рис. [-@fig:017])

![Настройка NAT на маршрутизаторе msk-donskaya-gw-1](image/17.png){#fig:017 width=70%}

# Выводы

В результате выполнения лабораторной работы было настроено взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.

# Контрольные вопросы

1. В каких случаях следует использовать статическую маршрутизацию? При-
ведите примеры.

Статическая маршрутизация - это метод, при котором сетевой администратор вручную настраивает маршруты в таблице маршрутизации устройства (например, маршрутизатора). Это отличается от динамической маршрутизации, где маршрутизаторы обмениваются информацией и автоматически обновляют свои таблицы маршрутизации.

Статическую маршрутизацию следует использовать в следующих случаях:

    Небольшие, простые сети: В сетях с небольшим количеством маршрутизаторов и предсказуемой топологией статическая маршрутизация может быть проще в настройке и управлении. Нет необходимости в сложных протоколах маршрутизации.
        Пример: Домашняя сеть с одним маршрутизатором, который подключается к интернету. Вы просто указываете маршрут по умолчанию через шлюз провайдера.

2. Укажите основные принципы статической маршрутизации между VLANs.

Маршрутизация между VLANs (Virtual Local Area Networks) необходима, потому что VLANs по своей природе разделяют широковещательные домены. Устройства в разных VLANs не могут общаться напрямую на втором уровне модели OSI (канальный уровень). Для связи между VLANs требуется устройство третьего уровня (сетевой уровень), обычно маршрутизатор или коммутатор третьего уровня.

