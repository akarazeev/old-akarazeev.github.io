---
title: Бот ipy2pdf
lang: ru
ref: botipy2pdf160513
date: 2016-05-13 03:00:01 +03:00
tags:
- MIPT
- Telegram💬
- Bot
- Jupyter
layout: post
header:
  teaser: "/images/ipy2pdf.jpg"
---

![image-center]({{ page.header.teaser }}){: .align-center}

[Проект на GitHub'e](https://github.com/akarazeevprojects/ipy2pdf)

## ipy2pdf

Этот скрипт позволяет конвертировать _notebook.ipynb_, который содержит кириллические символы, в _notebook.pdf_.

| Установка | Использование | На выходе |
| :-------------: | :-------------: | :-------------: |
| `python install.py` | `ipy2pdf notebook.ipynb` | `notebook.pdf` |

Это довольно просто

## Telegram-бот доступен по следующему адресу: [@ipynbot](https://t.me/ipynbot)

Просто отправь ему `notebook.ipynb`.

## Требования

На твоей машине должны быть установлены `pdflatex` и `jupyter`.

У меня на маке установлен [MacTeX](http://www.tug.org/mactex/).

## В случае возникновения проблем

Скрипт выполняет следующие команды:

1. `jupyter nbconvert <>.ipynb --to latex`
2. Добавляет строку `\usepackage[T2A]{fontenc}` сразу после `\usepackage[T1]{fontenc}`
3. `pdflatex -interaction=nonstopmode <>.tex`
4. Удаляет логи и временные файлы/директории

Буду рад любому фидбэку.
