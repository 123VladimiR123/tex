---
## Front matter
title: "Лабораторная работа №2"
subtitle: "Примеры функциональных возможностей Latex"
author: "Кубасов В.Ю., ст.б. 1132249516"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: false # List of figures
lot: false # List of tables
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
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

- Познакомиться с синтаксисом и возможностями Latex

# Задание

- Использовать базовый функционал Latex

# Теоретическое введение

The first document shows the basics. LaTeX documents are a mixture of text and
commands. The commands start with a backslash and sometimes have arguments
in curly braces (or sometimes optional arguments in square brackets). Then you
get an output PDF by telling LaTeX to typeset your file.

# Выполнение лабораторной работы

## Пример из ресурса

![Пример первого документа из книги](./image/image.png)

## Математические записи

![Формульная запись](./image/image%20copy.png)

## Параграф и жесткие пробелы

![Параграф и жесткие пробелы](./image/image%20copy%202.png)

## Нумерованный список

![Нумерованный список](./image/image%20copy%203.png)

## Разделы и подразделы

![Разделы и подразделы](./image/image%20copy%204.png)

# Выводы

![Итоговый вариант](./image/image%20copy%205.png)

# Список литературы{.unnumbered}

::: {#refs}
:::
