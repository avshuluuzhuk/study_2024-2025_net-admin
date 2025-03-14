---
## Front matter
title: "Первоначальное конфигурирование сети"
subtitle: "Лабораторная работа № 4"
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

Провести подготовительную работу по первоначальной настройке коммутаторов сети

# Задание

Требуется сделать первоначальную настройку коммутаторов сети, представленной на схеме L1 (см. рис. 3.1 из раздела 3.3). Под первоначальной настройкой понимается указание имени устройства, его IP-адреса, настройка доступа по паролю к виртуальным терминалам и консоли, настройка удалённого доступа к устройству по ssh.

# Выполнение лабораторной работы

В логической рабочей области Packet Tracer разместим коммутаторы и оконечные устройства согласно схеме сети L1 и соединим их через соответствующие интерфейсы (рис. [-@fig:001])

![Размещение коммутаторов и оконечных устройств согласно схеме сети L1](image/1.png){#fig:001 width=70%}

$$ a=b+c, $$ где \\( a=0 \\)

Используя типовую конфигурацию коммутатора, настроем все коммутаторы, изменяя название устройства и его IP-адрес согласно плану IP (рис. [-@fig:002]) (рис. [-@fig:003]) (рис. [-@fig:004]) (рис. [-@fig:005])  (рис. [-@fig:006])

![Последовательность команд по первоначальной настройке коммутатора msk-donskaya-sw-1](image/2.png){#fig:002 width=70%}

![Последовательность команд по первоначальной настройке коммутатора msk-donskaya-sw-2](image/3.png){#fig:003 width=70%}

![Последовательность команд по первоначальной настройке коммутатора msk-donskaya-sw-3](image/4.png){#fig:004 width=70%}

![Последовательность команд по первоначальной настройке коммутатора msk-donskaya-sw-4](image/5.png){#fig:005 width=70%}

![Последовательность команд по первоначальной настройке коммутатора msk-pavlovskaya-sw-1](image/6.png){#fig:006 width=70%}

# Выводы

В результате выполнения лабораторной работы провели подготовительную работу по первоначальной настройке коммутаторов сети

# Контрольные вопросы

1. При помощи каких команд можно посмотреть конфигурацию сетевого
оборудования?

Ответ: На устройствах Cisco: show running-config для просмотра текущей конфигурации и show startup-config для просмотра конфигурации, которая загружается при старте устройства.

2. При помощи каких команд можно посмотреть стартовый конфигурацион-
ный файл оборудования?

Ответ: На Cisco: show startup-config.

3. При помощи каких команд можно экспортировать конфигурационный файл
оборудования?

Ответ: На Cisco: copy running-config tftp: для копирования текущей конфигурации на TFTP-сервер или copy startup-config tftp: для копирования стартовой конфигурации.

4. При помощи каких команд можно импортировать конфигурационный файл
оборудования

Ответ: На Cisco: copy tftp: running-config для копирования конфигурации с TFTP-сервера на устройство или copy tftp: startup-config для загрузки конфигурации из TFTP-сервера в оперативную память.
