---
## Front matter
title: "Отчёт по лабораторной работе №4"
subtitle: "Дисциплина: Архитектура компьютера"
author: "Соснина Виктория Евгеньевна"

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

Цель данной работы --- изучение основ легковесного языка разметки Markdown для написания отчетов по лабораторным работам, получение навыка компиляции файлов и их загрузки на GitHub.

# Выполнение лабораторной работы

Перейдем в каталог курса, обновим локальный репозиторий, перейдем в каталог с шаблоном отчета по лабораторной работе №4.

![Переход к отчету №4](image/4_1.png){ #fig:001 width=70% }

Проведем компиляцию шаблона с помощью команды make. Проверим правильность выполненных действий с помощью команды ls. Удалим созданные файлы с помощью команды make clean. Снова проверим правильность действий с помощью команды ls.

![Компиляция шаблона отчета](image/4_2.png){ #fig:001 width=70% }

![Проверка правильности действий](image/4_3.png){ #fig:001 width=70% }

Откроем файл отчета с помощью текстового редактора (в данном случае мы использовали gedit)

![Открытие файла report.md](image/4_4.png){ #fig:001 width=70% }

Изучив структура файла, заполним отчет по лабораторной работе.

КАРТИНКА

Скомпилируем отчет в форматах pdf и docx.

КАРТИНКА

Загрузим файлы на GitHub.

КАРТИНКА

# Выполнение заданий для самостоятельной работы

Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию (рис. [-@fig:001])

![Название рисунка](image/placeimg_800_600_tech.jpg){ #fig:001 width=70% }

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
