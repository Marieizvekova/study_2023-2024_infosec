---
## Front matter
title: "Лабораторная работа №6"
subtitle: "Поиск файлов. Перенаправление
ввода-вывода. Просмотр запущенных процессов"
author: "Извекова Мария Петровна"

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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.

# Выполнение лабораторной работы

1. Записываем в файл file.txt  названия всех файлов которые находятся в домашнем каталоге и выводим на экран то, что записали (рис. @fig:001).

![рис. 1](image/1.jpg){#fig:001 width=70%}

2. Записываем в файл file.txt  названия всех файлов которые находятся в  каталоге /etc и выводим на экран то, что записали (рис. @fig:002 - @fig:003).

![рис. 2](image/2.jpg){#fig:002 width=70%}

![рис. 3](image/3.jpg){#fig:003 width=70%}

3.  в файл conf.txt записываем файлы с расширением .conf из каталога /etc (рис. @fig:004).

![рис. 4](image/4.jpg){#fig:004 width=70%}

выводим на экран то, что записалось в файл (рис. @fig:005).

![рис. 5](image/5.jpg){#fig:005 width=70%}

4. выводим на экран все файлы из каталога /etс, которые начинаются с h
(рис. @fig:006)

![рис. 6](image/6.jpg){#fig:006 width=70%}

то что получилось (рис. @fig:007)

![рис. 7](image/7.jpg){#fig:007 width=70%}

5. Запускаем в фоновом режиме процесс, который будет записывать в файл ~/logfile
файлы, имена которых начинаются с log (рис. @fig:008)

![рис. 8](image/8.jpg){#fig:008 width=70%}

результат (рис. @fig:009)

![рис. 9](image/9.jpg){#fig:009 width=70%}

удаляем файл logfile (рис. @fig:010)

![рис. 10](image/10.jpg){#fig:010 width=70%}

6. в фоновом режиме запускаем текстовый редактор (рис. @fig:011)

![рис. 11](image/11.jpg){#fig:011 width=70%}

Определяем идентификатор процесса gedit, используя команду ps, конвейер и фильтр
grep.  (рис. @fig:012)

![рис. 12](image/12.jpg){#fig:012 width=70%}

Завершаем процесс (рис. @fig:013)

![рис. 13](image/13.jpg){#fig:013 width=70%}

7. с помощью команды man определяем функции команд df, du (рис. @fig:014 -  @fig:015)

![рис. 14](image/14.jpg){#fig:014 width=70%}

![рис. 15](image/15.jpg){#fig:015 width=70%}

8. выполняем эти команды (рис. @fig:016)

![рис. 16](image/16.jpg){#fig:016 width=70%}

9. Воспользовавшись справкой команды find, выводим имена всех директорий, имею-
щихся в вашем домашнем каталоге. (рис. @fig:017)

![рис. 17](image/17.jpg){#fig:017 width=70%}


# Контрольные вопросы

1. stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый дескриптор
0;
– stdout — стандартный поток вывода (по умолчанию: консоль), файловый дескриптор
1;
– stderr — стандартный поток вывод сообщений об ошибках (по умолчанию: консоль),
файловый дескриптор 2.

2. > - перенаправление
>> - открытие файла в режиме добавления

3. Конвейер (pipe) служит для объединения простых команд или утилит в цепочки, в которых результат работы предыдущей команды передаётся последующей. 

4. Любой команде, выполняемой в системе, присваивается идентификатор процесса
(process ID). 

5. Запущенные фоном программы называются задачами (jobs). Ими можно управлять
с помощью команды jobs, которая выводит список запущенных в данный момент задач

6. top - display Linux processes

7. find - команда по поискам файлов.
8. удалить процесс можно с помощью команды kill+ название процесса.

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
