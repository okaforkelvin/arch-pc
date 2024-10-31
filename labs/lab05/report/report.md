---
## Front matter
title: "Отчёт по лабораторной работе 5"
subtitle: "Основы работы с Midnight Commander. Структура программы на языке ассемблера NASM. Системные вызовы в ОС GNU Linux"
author: "Окафор Чуквуемезуго Келвин"

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

Целью работы является приобретение практических навыков работы в Midnight Commander, а также освоение инструкций языка ассемблера mov и int.

# Выполнение лабораторной работы

## Знакомство с Midnight Commander

Я запустил Midnight Commander и, используя стрелочные клавиши и клавишу Enter, перешел в каталог ~/work/arch-pc. Затем нажал F7 для создания нового каталога lab05.

![Запуск Midnight Commander](image/01.png){ #fig:001 width=70%, height=70% }

![Создание каталога lab05](image/02.png){ #fig:002 width=70%, height=70% }

С помощью команды touch я создал файл lab05-1.asm.

![Создание файла lab05-1.asm](image/03.png){ #fig:003 width=70%, height=70% }

Я открыл файл для редактирования, нажав F4, выбрал редактор mceditor и написал код программы в соответствии с заданием.

![Редактирование программы в файле lab05-1.asm](image/04.png){ #fig:004 width=70%, height=70% }

Для проверки я открыл файл на просмотр, нажав F3, и убедился, что он содержит правильный код.

![Просмотр содержимого файла lab05-1.asm](image/05.png){ #fig:005 width=70%, height=70% }

Я скомпилировал программу, сгенерировал объектный файл, произвел компоновку и запустил исполняемый файл, чтобы убедиться в корректности работы.

![Запуск программы lab05-1.asm](image/06.png){ #fig:006 width=70%, height=70% }

## Подключение внешнего файла in_out.asm

Я скачал файл in_out.asm и разместил его в рабочем каталоге. Для копирования использовал клавишу F5, а для перемещения — клавишу F6.

![Копирование файла in_out.asm в рабочий каталог](image/07.png){ #fig:007 width=70%, height=70% }

Я также скопировал файл lab05-1.asm в новый файл lab05-2.asm.

![Копирование файла lab05-1.asm в lab05-2.asm](image/08.png){ #fig:008 width=70%, height=70% }

В файле lab05-2.asm я написал код программы, используя подпрограммы из внешнего файла in_out.asm. Программа была успешно скомпилирована и протестирована.

![Программа в файле lab05-2.asm](image/09.png){ #fig:009 width=70%, height=70% }

![Запуск программы lab05-2.asm](image/10.png){ #fig:010 width=70%, height=70% }

В файле lab05-2.asm я заменил подпрограмму sprintLF на sprint. После пересборки исполняемого файла вывод строки больше не завершается символом новой строки.

![Обновленная программа в lab05-2.asm](image/11.png){ #fig:011 width=70%, height=70% }

![Запуск обновленной программы lab05-2.asm](image/12.png){ #fig:012 width=70%, height=70% }

## Задание для самостоятельной работы

Я скопировал программу lab05-1.asm и изменил код так, чтобы он работал по следующему алгоритму:

* вывести приглашение с текстом “Введите строку:”;
* считать строку с клавиатуры;
* вывести введённую строку на экран.

![Копирование файла lab05-1.asm для нового задания](image/13.png){ #fig:013 width=70%, height=70% }

![Код программы в файле lab05-3.asm](image/14.png){ #fig:014 width=70%, height=70% }

![Запуск программы lab05-3.asm](image/15.png){ #fig:015 width=70%, height=70% }

Аналогично, я скопировал программу lab05-2.asm и внес изменения в код, теперь используя подпрограммы из файла in_out.asm.

![Копирование файла lab05-2.asm для модификации](image/16.png){ #fig:016 width=70%, height=70% }

![Код программы в файле lab05-4.asm](image/17.png){ #fig:017 width=70%, height=70% }

![Запуск программы lab05-4.asm](image/18.png){ #fig:018 width=70%, height=70% }

# Выводы

Я научился писать базовые ассемблерные программы и освоил ассемблерные инструкции mov и int.
