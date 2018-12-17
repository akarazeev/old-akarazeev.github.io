---
title: ipy2pdf Bot
lang: ru
ref: botipy2pdf160513
date: 2016-05-13 03:00:01 +03:00
tags:
- MIPT
- Telegram
- Bot
- Jupyter
layout: post
header:
  teaser: "/assets/images/ipy2pdf.jpg"
---

![image-center]({{ page.header.teaser }}){: .align-center}

[Project](https://github.com/akarazeevprojects/ipy2pdf)

## ipy2pdf

Script to convert _notebook.ipynb_, containing russian/cyrrilic symbols, into _notebook.pdf_.

| Installation | Usage | Output |
| :-------------: | :-------------: | :-------------: |
| `python install.py` | `ipy2pdf notebook.ipynb` | `notebook.pdf` |

That's easy.

## Telegram-bot is available at [@ipynbot](https://t.me/ipynbot)

Just send `notebook.ipynb` to him.

## Requirements

You need to have `pdflatex` already installed on your system. And of course `jupyter`.

On my system I have [MacTeX](http://www.tug.org/mactex/) installed.

## In case of troubles

This script executes following commands:

1. `jupyter nbconvert <>.ipynb --to latex`
2. Add line `\usepackage[T2A]{fontenc}` after `\usepackage[T1]{fontenc}`
3. `pdflatex -interaction=nonstopmode <>.tex`
4. Removes some logs and temporary files/directories

I appreciate any kind of feedback.
