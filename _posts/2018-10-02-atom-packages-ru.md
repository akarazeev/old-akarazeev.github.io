---
title: Пакеты для текстового редактора Atom
lang: ru
ref: atompackages181002
date: 2018-10-02 18:00:00 +03:00
tags:
- Atom
- Text Editor
- Programming
- Packages
layout: post
header:
  teaser: "/assets/images/atom.jpeg"
---

![image-center]({{ page.header.teaser }}){: .align-center}

Текстовым редактором [Atom](https://atom.io) я пользуюсь уже давно, поэтому решил написать про него пару слов.

Одно из первых, что мне в нём понравилось -- он полностью опенсурсный. Исходники можно найти в [соответствующем репозитории](https://github.com/atom/atom). А также возможность расширения его функционала различными пакетами убедила меня перейти на него.

Я решил записать список пакетов, которые я уже "насобирал" за время пользования этим редактором: [atom-packages.txt](/data/atom-packages.txt).

После установки самого Atom'a, установить пакеты из файла "atom-packages.txt" можно в одну команду: `apm install --packages-file atom-packages.txt`

А с помощью этой команды я записывал список установленных пакетов в файл "atom-packages.txt": `apm list --installed --bare > atom-packages.txt`.

Проверка правописания для русского и английского языков: `Cmd + ,` -> `Packages` -> Найти "spell-check" -> `Settings` -> Установить значение “en-US, ru-RU” у поля `Locales` (так происходит настройка любого установленного пакета).

Часть пакетов предполагают наличие установленных соответствующих питоновских библиотек (например, `pycodestyle`). Почти наверное, достаточным будет выполнить следующие команды:
```
pip install --upgrade pycodestyle
pip install --upgrade pyflakes
pip install --upgrade mypy
```

Пару слов про [MyPy](http://mypy-lang.org/index.html): инструмент, который проводит статическую проверку типизации (подробнее можно почитать на их сайте, там и примеры есть). Чтобы избежать большого количества `предупреждений` в проектах, где за типизацией особо следить не приходится, я убрал галочки с со следующих пунктов в настройках пакета `linter-mypy`: `Disallow Untyped Defs`, `Disallow Any Expr` и `Warn Missing Imports`.

Темы, которые я использую: оба поля -- `UI Theme` и `Syntax Theme` -- имеют значение “One Light”.
