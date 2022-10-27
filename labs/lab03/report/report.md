---
## Front matter
title: "Отчёт по лабораторной работе №3"
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

Цель данной работы – получение практических навыков работы с системой
git, изучение средств контроля версий.

# Выполнение лабораторной работы

## Настройка github

Создадим учетную запись на https://github.com/

![Создание учетной записи на github](image/3_1.png){ #fig:001 width=70% }

## Базовая настройка git

Укажем имя и адрес электронной почты. Эта информация не может быть изменена и будет доступна при каждом внесенном изменении в проект. Используем для этого команды git config --global user.name и git config --global user.email. Также настроим utf-8 в выводе сообщений git с помощью команды git config --global core.quotepath false.

![Начальная настройка git](image/3_2.png){ #fig:002 width=70% }

Назовем начальную ветку master, введем параметры autocrlf и safecrlf.

![Создание начальной ветки](image/3_3.png){ #fig:003 width=70% }

## Создание SSH ключа

Сгенерируем приватный и открытый (public) ключи. Они необходимы для идентификации пользователя на сервере репозиториев. Используем для этого команду ssh-keygen -C. Сгенерированные ключи хранятся в каталоге ~/.ssh/. Скопируем в буфер обмена публичный ключ, получив к нему доступ с помощью команды cat.

![Создание SSH ключа](image/3_4.png){ #fig:004 width=70% }

Загрузим открытый ключ в github и зададим ему имя.

![Загрузка ключа на github](image/3_5.png){ #fig:005 width=70% }

![Лист SSH ключей](image/3_6.png){ #fig:006 width=70% }

## Сознание рабочего пространства и репозитория курса на основе шаблона

Откроем терминал и создадим каталог для дисциплины «Архитектура компьютеров», используя команду mkdir.

![Создание каталога «Архитектура компьютера»](image/3_7.png){ #fig:007 width=70% }

## Сознание репозитория курса на основе шаблона

Через web-интерфейс github создадим репозиторий на основе шаблона,размещенного на странице https://github.com/yamadharma/course-directory-student-template. Используем шаблон, нажав “Use this template”. study_2022–2023_arh-pc

![Использование шаблона для репозитория](image/3_8.png){ #fig:008 width=70% }

Создадим репозиторий на основе данного шаблона и назовем его study_2022–2023_arh-pc.

![Создание шаблона репозитория](image/3_9.png){ #fig:009 width=70% }

Через терминал перейдем в созданный нами каталог курса, используя команду cd. Клонируем его в созданный репозиторий с помощью команды git clone,предварительно скопировав ссылку для клонирования.

![Копирование ссылки для клонирования](image/3_10.png){ #fig:010 width=70% }

![Клонирование репозитория](image/3_11_1.png){ #fig:011 width=70% }

![Клонирование репозитория](image/3_11_2.png){ #fig:012 width=70% }

## Настройка каталога курса

Через терминал перейдём в каталог курса, используя команду cd. Удалим лишние файлы и создадим необходимые каталоги, отправим файлы на сервер.

![Удаление лишних файлов, отправка на сервер](image/3_12_1.png){ #fig:013 width=70% }

![Удаление лишних файлов, отправка на сервер](image/3_12_2.png){ #fig:014 width=70% }


Проверим правильность создания иерархии рабочего пространства как в локальном репозитории, так и на странице github.

![Проверка иерархии в локальном репозитории](image/3_13.png){ #fig:015 width=70% }

![Проверка иерархии на github](image/3_14.png){ #fig:016 width=70% }

Выполнение заданий, описанных выше, позволило нам научиться создавать учетную запись на github, выполнять базовую настройку git, создавать приватные и открытые ключи, создавать рабочее пространство репозитория, использовать существующий шаблон репозитория.

# Выполнение заданий для самостоятельной работы

Создадим отчет по выполнению текущей лабораторной работы в соответствующем каталоге рабочего пространства (labs/lab03/report).

![Создание файла отчета](image/3_15.png){ #fig:017 width=70% }

Скопируем отчеты по выполнению предыдущих лабораторных работ в соответствующие каталоги созданного рабочего пространства.

![Копирование отчетов предыдущих лабораторных работ](image/3_16.png){ #fig:018 width=70% }

Загрузим файлы на github, используя команды git add ., git commit, git push.

![Загрузка изменений на github](image/3_17.png){ #fig:019 width=70% }

Выполнение заданий для самостоятельной работы позволило нам научиться загружать отчеты лабораторных работ на сервер.

# Вывод

В результате выполнения лабораторной работы я получила практические навыки по работе с системой git, изучила и применила средства контроля версий, что потребуется для дальнейшей работы на курсе.

# Список литературы{.unnumbered}

::: {#refs}
:::
