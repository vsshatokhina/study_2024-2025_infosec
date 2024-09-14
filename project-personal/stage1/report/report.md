---
## Front matter
title: "Отчет по проекту"
subtitle: "Этап 1"
author: "Шатохина Виктория Сергеевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"
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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Знакомство с дистрибутивом Kali Linux.

# Выполнение лабораторной работы

**1.** Скачала сайт Kali Linux образ.

**2.** Настроила виртуальную машину. (рис. [-@fig:002]) (рис. [-@fig:003]) (рис. [-@fig:004]) (рис. [-@fig:005])

![Язык](image/2.png){ #fig:002 width=60% }

![Местонахождение](image/3.png){ #fig:003 width=60% }

![Клавиатура](image/4.png){ #fig:004 width=60% }

![Сеть](image/5.png){ #fig:005 width=60% }

**3.** Задала учетные данные. (рис. [-@fig:006])

![Учетная запись](image/6.png){ #fig:006 width=60% }

**4.** Перезапустила и зашла под учеткой. (рис. [-@fig:007])

![Kali](image/7.png){ #fig:007 width=60% }

# Вывод

Я познакомилась дистрибутивом Kali Linux.
