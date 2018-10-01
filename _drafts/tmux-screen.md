---
title: tmux vs screen
date: 2018-10-03 18:00:00 +03:00
tags:
- Terminal
- Command Line
- Programming
- Commands
layout: single
---

Hm, well, when you want to run some script or service on start up you better use `screen` command.

The main reason is that `tmux` can’t be launched on start up (without user’s login).

The syntax is pretty simple:

1. Запустить последовательность команд в фоне: `screen -dmS <screen_name> bash -c “<command1>; <command2>; <command3>;”`
2. Запустить команду в фоне: `screen -dmS <screen_name> “<command>”`
3. Закрыть запущенную программу в окне <screen_name>: `screen -S <screen_name> -X quit`
