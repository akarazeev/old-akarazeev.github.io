---
title: tmux vs screen
date: 2018-10-06 06:00:00 +03:00
tags:
- Terminal
- Command Line
- Programming
- Commands
layout: single
---

![image-center]({{ page.header.teaser }}){: .align-center}

Due to I have many services and servers on **Raspberry Pi** I need to spend some time after turning on and realaunching the RPi to start every service and server.

I emerged that **screen** is pretty good solution to my problem because it allows to run scripts and programs on boot of device[^1].

[^1]: Running the scripts and programs in background on boot at [`homebridge` repository](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen)

Before this I was always using **tmux** but its functionality doesn't allow doing so -- user has to login to launch every script and program in background **tmux**-sessions like I needed.

About **tmux**:
- Create new session:
```
tmux new -s <name>
```
- Hide the session (detach from it): `Ctrl+B` then `D`
- List all sessions:
```
tmux ls
```
- Attach to session:
```
tmux a -t <name>
```
- Close the session: `Ctrl+B` then `X`


About **screen**:
- Run the command on background:
```
screen -dmS <screen_name> "<command>"
```
- Run the sequence of programs in background:
```
screen -dmS <screen_name> bash -c "<command1>; <command2>; <command3>;"
```
- Hide the session (detach from it): `Ctrl+A` then `D`
- List all sessions:
```
screen -list
```
- Attach to session:
```
screen -x <screen_name>
```
- Close running in `<screen_name>` program:
```
screen -S <screen_name> -X quit
```

---

1. Running the scripts and programs in background on boot at [`homebridge` repository](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen)
2. More about [`screen` command](https://help.ubuntu.ru/wiki/screen) on Ubuntu
3. [tmux vs screen](https://www.reddit.com/r/linux/comments/6ffrmy/differences_between_tmux_vs_screen/) on Reddit'e
