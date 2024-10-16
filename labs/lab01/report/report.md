---
## Front matter
title: "Отчет по лабораторной работе № 1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Шатохина Виктория Сергеевна"


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
#lot: true # List of tables
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Теоретическое введение

Программа VirtualBox предоставляет широкий спектр возможностей для работы с виртуальными машинами. Это решение подходит для тестирования новых операционных систем, запуска старых приложений или изоляции потенциально опасного программного обеспечения. Благодаря интуитивно понятному интерфейсу и богатому функционалу, VirtualBox стал выбором многих пользователей по всему миру[1].

# Выполнение лабораторной работы

Запускаем виртуальную машину, нажимаем кнопку "создать" и выбираем скаченный образ ISO: Cм. [рис. 1](#fig:001)

![Создание виртуальной машины](image/1.png){ #fig:001 width=70% }

Настраиваем оборудование ВМ, изменяя размер ОЗУ: Cм. [рис. 3](#fig:003)

![Оборудование VB](image/3.png){ #fig:003 width=70% }

Создаём новый виртуальный жёсткий диск размером 40 Гб: Cм. [рис. 4](#fig:004)

![Размер памяти](image/4.png){ #fig:004 width=70% }

Проверям итоговую конфигурацию для виртуальной машины: Cм. [рис. 5](#fig:005)

![Итоговые настройки](image/5.png){ #fig:005 width=70% }

Меняем контроллер на скаченный образ Rocky: Cм. [рис. 6](#fig:006)

![Носители](image/6.PNG){ #fig:006 width=70% }

Попадаем в стартовое меню установки, выбираем русский язык: Cм. [рис. 7](#fig:007)

![Стартовое меню установки](image/7.png){ #fig:007 width=70% }

В Installation Destination выбираем диск: Cм. [рис. 8](#fig:008)

![Выбор диска](image/8.png){ #fig:008 width=70% }

В Softwear Selection выбираем Server with GUI. В дополнительном ПО отмечаем Development Tools: Cм. [рис. 9](#fig:009)

![Server with GUI](image/9.png){ #fig:009 width=70% }

Заходим в KDUMP и отключаем его: Cм. [рис. 10](#fig:010)

![Отключение KDUMP](image/10.png){ #fig:010 width=70% }

Заходим в Network&Host Name и прописываем host name: Cм. [рис. 11](#fig:011)

![Имя хоста](image/11.png){ #fig:011 width=70% }

В разделе Root Password задаём пароль: Cм. [рис. 12](#fig:012)

![Root password](image/12.png){ #fig:012 width=70% }

Завершаем настройки во вкладке Create User: Cм. [рис. 13](#fig:013)

![Create User](image/13.png){ #fig:013 width=70% }

Запускаем установку и дожидаемся перезагрузки системы: Cм. [рис. 14](#fig:014)

![Завершение установки](image/14.png){ #fig:014 width=70% }

Заходим в созданный аккаунт: Cм. [рис. 15](#fig:015)

![Вход в аккаунт](image/15.png){ #fig:015 width=70% }

Запускаем образ диска дополнений гостевой ОС: Cм. [рис. 16](#fig:016)

![Подключение гостевых настроек](image/16.png){ #fig:016 width=70% }

# Домашнее задание

Просмотрим последовательность загрузки системы, выполнив команду dmesg: Cм. [рис. 17](#fig:017)

![Последовательность загрузки системы](image/17.png){ #fig:017 width=70% }

Получим следующую информацию:  Cм. [рис. 18](#fig:018),  Cм. [рис. 19](#fig:019), Cм. [рис. 20](#fig:020),  Cм. [рис. 21](#fig:021)

1. Версия ядра Linux (Linux version).
2. Частота процессора (Detected Mhz processor).
3. Модель процессора (CPU0).
4. Объем доступной оперативной памяти (Memory available).
5. Тип обнаруженного гипервизора (Hypervisor detected).
6. Тип файловой системы корневого раздела.
7. Последовательность монтирования файловых систем

![Версия ядра Linux, частота процессора, модель процессора](image/18.png){ #fig:018 width=70% }

![Объем доступной оперативной памяти ](image/19.png){ #fig:019 width=70% }

![Тип обнаруженного гипервизора, тип файловой системы корневого раздела ](image/20.png){ #fig:020 width=70% }


# Заключение

Приобрели практические навыки установки операционной системы на виртуальную машину, настроили минимально необходимые для дальнейшей работы сервисы.

# Ответы на вопросы

1. Какую информацию содержит учётная запись пользователя?

Учётная запись пользователя в Linux содержит следующую информацию:

- Имя пользователя (username) — уникальное имя пользователя в системе.

- Идентификатор пользователя (UID) — уникальный числовой идентификатор для каждого пользователя.

- Идентификатор группы (GID) — идентификатор основной группы, к которой принадлежит пользователь.

- Домашний каталог (home directory) — директория, в которой пользователь хранит свои файлы и настройки.

- Интерпретатор команд (shell) — программа, запускаемая по умолчанию при входе пользователя в систему.

- Пароль пользователя — обычно хранится в хешированном виде в файле /etc/shadow.

Эти данные обычно содержатся в файле /etc/passwd, а зашифрованные пароли — в файле /etc/shadow.

2. Укажите команды терминала и приведите примеры:
– для получения справки по команде;

– для перемещения по файловой системе;

– для просмотра содержимого каталога;

– для определения объёма каталога;

– для создания / удаления каталогов / файлов;

– для задания определённых прав на файл / каталог;

– для просмотра истории команд.

Для получения справки по команде: man <имя_команды>
Пример: man ls — получить справку по команде ls.

Для перемещения по файловой системе: cd <путь_к_каталогу>
Пример: cd /home/user — перейти в каталог /home/user.

Для просмотра содержимого каталога: ls [опции] <путь_к_каталогу>
Пример: ls -la /home/user — показать все файлы и каталоги, включая скрытые, с подробной информацией.

Для определения объёма каталога: du -sh <путь_к_каталогу>
Пример: du -sh /home/user — показать общий размер каталога /home/user.

Для создания / удаления каталогов / файлов:

mkdir <имя_каталога> - Создание каталога

rmdir <имя_каталога> - Удаление пустого каталога

touch <имя_файла> - Создание пустого файла

rm <имя_файла> - Удаление файла

rm -r <имя_каталога> - Рекурсивное удаление каталога и его содержимого

Примеры:

    mkdir new_folder

    touch new_file.txt

    rm new_file.txt

    rm -r new_folder

Для задания определённых прав на файл / каталог: chmod <права> <имя_файла_или_каталога>

Пример: chmod 755 script.sh — установить права rwxr-xr-x на файл script.sh.

Для просмотра истории команд: history

3. Что такое файловая система? Приведите примеры с краткой характеристикой.

Файловая система — это метод и структура, по которым данные хранятся, организуются и управляются на носителе информации (жесткий диск, SSD, USB-накопитель и т.д.).

Примеры файловых систем:

EXT4 (Fourth Extended Filesystem): Одна из самых популярных файловых систем в Linux. Поддерживает журналирование, большие объемы данных, улучшенную производительность. Хорошо подходит для большинства стандартных Linux-установок.

NTFS (New Technology File System): Файловая система, используемая в операционных системах Windows. Поддерживает большие файлы, разрешения, шифрование и сжатие. 

FAT32 (File Allocation Table 32): Универсальная файловая система, поддерживаемая практически всеми операционными системами.
Ограничение на размер файла — до 4 ГБ.

XFS: Журналируемая файловая система с высокой производительностью, разработанная для систем с большими объемами данных.
Хорошо подходит для серверных систем и больших файловых хранилищ.

ZFS: Передовая файловая система, поддерживающая большой объем данных, снапшоты, клонирование и защиту данных. Разработана для высоконадежных систем.

4. Как посмотреть, какие файловые системы подмонтированы в ОС?

Чтобы посмотреть, какие файловые системы подмонтированы в операционной системе Linux, можно воспользоваться несколькими способами. Во-первых, можно использовать команду mount, которая выводит список всех текущих монтированных файловых систем, их устройства, точки монтирования, типы файловых систем и параметры монтирования. Например, при вводе команды mount в терминале вы получите информацию о том, какие файловые системы были смонтированы и в каком порядке.

Во-вторых, можно просмотреть содержимое файла /proc/mounts, который также содержит сведения о всех монтированных файловых системах, включая псевдо-файловые системы вроде proc и sysfs. Это можно сделать, выполнив команду cat /proc/mounts в терминале. Наконец, команду df -h можно использовать для отображения информации о свободном и занятом пространстве на смонтированных файловых системах, что может быть полезным для мониторинга состояния системы.

5. Как удалить зависший процесс?

Для удаления зависшего процесса в Linux сначала нужно определить его идентификатор (PID). Это можно сделать с помощью команды ps aux, которая выводит список всех запущенных процессов в системе вместе с их PID, или с помощью утилит top или htop, которые предоставляют интерактивный список процессов.

После того как PID зависшего процесса известен, можно использовать команду kill <PID> для отправки сигнала завершения процессу. Если процесс не реагирует на обычный сигнал завершения, его можно принудительно завершить, используя команду kill -9 <PID>. Этот сигнал (-9) немедленно завершает процесс, игнорируя любые попытки его сохранения или корректного завершения.

# Библиографическая справка 

[1] Документация по VirtualBox: https://www.virtualbox.org/

