---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Images, floats, hyperrefs"
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

- Научиться выравниванию
- Овладеть навыками картинок

# Задание
- Попробуйте включить созданное вами изображение, заменив «стандартные», которые мы
использовали в демонстрации.
- Изучите возможности клавиш высоты, ширины, угла и масштаба.
- Используйте клавишу ширины, чтобы задать размер графического элемента относительно ширины текста, а
другого графического элемента относительно ширины строки. Попробуйте, как они ведут себя с опцией «два столбца» и без неё.
- Используйте Lipsum для создания достаточно длинной демонстрации, а затем попробуйте разместить
плавающие элементы с помощью различных спецификаторов положения. Как взаимодействуют
различные спецификаторы?
- Попробуйте добавить новые пронумерованные части (разделы, подразделы, нумерованные списки)
в тестовый документ и выяснить, сколько запусков потребуется для работы
команд с метками.
- Добавьте несколько плавающих элементов и посмотрите, что произойдёт, если поставить метку перед
заголовком, а не после; можете ли вы предсказать результат?
- Что произойдёт, если поставить метку для уравнения после end?

# Теоретическое введение

Чтобы добавить графику извне LaTeX, используйте пакет graphicx, который добавляет
команду includegraphics в LaTeX. Вы можете включать файлы EPS, PNG, JPG и PDF. Если у вас несколько версий
графики, вы можете написать, например, example-image.png. (Пакет graphicx
попытается угадать расширение, если вы его не укажете.)
Вы заметите, что мы использовали здесь новое окружение, center, чтобы разместить изображение
горизонтально по центру страницы. Чуть позже мы подробнее поговорим о интервалах и
позиционировании.

# Выполнение лабораторной работы

```tex
\documentclass{article}

\usepackage[utf8]{inputenc}  
\usepackage[T2A]{fontenc}     
\usepackage[russian]{babel} 
\usepackage{graphicx}
\usepackage{multicol}
\usepackage[hidelinks]{hyperref}
\usepackage{lipsum} 
\graphicspath{{img/}}

\begin{document}
Pic height~\ref{sec:biba}
\begin{center}
\includegraphics[height = 0.5\textheight]{image.png}
\end{center}
\section{ABABABA}
\label{sec:biba}
\section{At the world starts}

\pagebreak


\begin{center}
\includegraphics[width = 0.5\linewidth]{image.png}
\end{center}

\pagebreak

Pic scale
\begin{center}
\includegraphics[scale = 0.2]{image.png}
\end{center}

\pagebreak

Pic angle
\begin{center}
\includegraphics[angle = 90, scale = 0.5]{image.png}
\end{center}

\pagebreak

Two column option
\begin{multicols}{2}
\includegraphics[height = 0.2\linewidth]{image.png}
\includegraphics[height = 0.2\textheight]{image.png}
\end{multicols}

\pagebreak
\lipsum[1-4]
\begin{figure}[ht]
\begin{center}
\label{figure:image}
\includegraphics[height = 0.5\textheight]{image.png}    
\caption{An example image}
\end{center}
\end{figure}

\lipsum[5-15]
link~\ref{figure:image}

\begin{equation}
e^{i\pi}+1 = 0
\label{eq:labeltwo}
\end{equation}

link~\ref{eq:labeltwo}

\end{document}
```

# Выводы

- Научились позиционировать и вставлять изображения в текст
- Овладели навыками базовой обработки формата изображения
- Освоили управление гиперссылками в документе

# Список литературы{.unnumbered}

::: {#refs}
:::
