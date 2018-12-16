---
title: tmux vs screen
date: 2018-10-06 06:00:00 +03:00
tags:
- Terminal
- Command Line
- Programming
- Commands
layout: single
header:
  teaser: "/assets/images/tmux.jpg"
lang: ru
ref: tmux181006
---

![image-center]({{ page.header.teaser }}){: .align-center}

Ввиду того, что у меня несколько сервисов и серверов на **Raspberry Pi**, после перезагрузки и включения этого устройства мне приходилось тратить некоторое время на то, чтобы всё поднять.

Решением этой проблемы оказалось использование команды **screen**, с помощью которой можно запускать заданные скрипты и программы при включении устройства[^1].

[^1]: Про запуск скриптов и программ в фоне в [репозитории `homebridge`](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen)

До этого я всегда пользовался **tmux**, но его так настроить нельзя -- нужно было именно логиниться в устройстве, чтобы все прописанные программы запустились в **tmux**-сессиях.

Про **tmux**:
- Создать новую сессию:
```
tmux new -s <name>
```
- Cкрыть сессию (выйти из неё): `Ctrl+B` затем `D`
- Список сессий:
```
tmux ls
```
- Присоединиться к сессии:
```
tmux a -t <name>
```
- Закрыть сессию: `Ctrl+B` затем `X`


Про **screen**:
- Запустить команду в фоне:
```
screen -dmS <screen_name> "<command>"
```
- Запустить последовательность команд в фоне:
```
screen -dmS <screen_name> bash -c "<command1>; <command2>; <command3>;"
```
- Cкрыть сессию (выйти из неё): `Ctrl+A` затем `D`
- Список сессий:
```
screen -list
```
- Присоединиться к сессии:
```
screen -x <screen_name>
```
- Закрыть запущенную программу в окне `<screen_name>`:
```
screen -S <screen_name> -X quit
```

---

1. Про запуск скриптов и программ в фоне в [репозитории `homebridge`](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen)
2. Подробнее про команду [`screen`](https://help.ubuntu.ru/wiki/screen) на Ubuntu
3. [tmux vs screen](https://www.reddit.com/r/linux/comments/6ffrmy/differences_between_tmux_vs_screen/) на Reddit'e
