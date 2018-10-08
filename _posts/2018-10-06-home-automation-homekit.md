---
title: Автоматизация Дома с Помощью Raspberry Pi и HomeKit
date: 2018-10-06 09:00:00 +03:00
tags:
- Raspberry Pi
- Home Automation
- HomeKit
- Apple
layout: single
header:
  teaser: "/assets/images/rpi-homekit.png"
gallery1:
  - url: /assets/images/home-ios-add.jpg
    image_path: /assets/images/home-ios-add.jpg
    title: "Подключение нового устройства"
  - url: /assets/images/home-ios-main.jpg
    image_path: assets/images/home-ios-main.jpg
    title: "Главный экран в приложении Home"
  - url: /assets/images/home-ios-office.jpg
    image_path: /assets/images/home-ios-office.jpg
  - url: /assets/images/home-ios-dining.jpg
    image_path: assets/images/home-ios-dining.jpg
  - url: /assets/images/home-ios-automation.jpg
    image_path: /assets/images/home-ios-automation.jpg
gallery2:
  - url: /assets/images/home-mac-main.jpg
    image_path: assets/images/home-mac-main.jpg
  - url: /assets/images/home-mac-office.jpg
    image_path: /assets/images/home-mac-office.jpg
  - url: /assets/images/home-mac-dining.jpg
    image_path: assets/images/home-mac-dining.jpg
  - url: /assets/images/home-mac-automation.jpg
    image_path: /assets/images/home-mac-automation.jpg
---

![image-center]({{ page.header.teaser }}){: .align-center}

### Зачем мы всё это делаем?

Цель этого поста -- показать как можно поставить [`homebridge`](https://github.com/nfarina/homebridge) сервер на **Raspberry Pi**. Этот сервер позволит управлять через приложение **Home** (на iOS и macOS) подключенными к **Raspberry Pi** устройствами (лампочками, вентиляторами, etc.)

Возможно, тебе будет интересно как я [делал "коробочку" с реле](https://akarazeev.github.io/proj_homeautomation/), которой можно управлять до 4ёх устройств.

{% include gallery id='gallery1' caption="Подключение нового устройства и обзор приложения Home на iOS" %}

{% include gallery id='gallery2' caption="Обзор программы Home на macOS" %}

---

### Начнём

Прежде всего нам потребуется установить ОС на RPi. Ставить будем Raspbian. Скачиваем торрент-файл с [официального сайта](https://www.raspberrypi.org/downloads/raspbian/) с помощью торрент-менеджера (я использовал [Transmission](https://transmissionbt.com)):

![alt](/assets/images/torrent.jpg)

**На всякий случай!** Для своего RPi я использую "lite" версию, потому что она занимает меньше места (в ней отсутствует визуальный интерфейс, который мне не нужен).
{: .notice--warning}

Затем разархивируем скачанный файл, чтобы получить сам образ -- файл `.img`. Для создания загрузочной microSD флешки я использовал приложение [Etcher](https://etcher.io):

![alt](/assets/images/etcher.jpg){: .align-center}

![alt](/assets/images/sdcard.jpg){: .align-right} После завершения процесса записи вынимаем карточку и вставляем в RPi. Нам потребуется клавиатура и монитор, чтобы провести первую настройку. Затем можно будет подключаться с помощью `ssh` к RPi.

**На всякий случай!** Мне удалось уместить всё необходимое на microSD с объёмом памяти в 2GB.
{: .notice--warning}

При первом подключении надо будет ввести "pi" в качестве `username` и "raspberry" в качестве `password`.

### Настройка Wi-Fi Соединения:

1. `sudo raspi-config`
2. "2. Network Options"
3. "N2. Wi-fi"
4. Choose your country
5. Enter the SSID (name) of your network
6. Enter the passphrase (password)
7. Press "Finish" button

Теперь RPi подключён к сети Wi-Fi. Это можно проверить с помощью `ping google.com` -- должно быть "0% packet loss".

### SSH

1. `sudo raspi-config`
2. "5. Interfacing Options"
3. "P2. SSH"
4. "Yes"
5. "Ok"
6. Press "Finish" button

---

### Установка homebridge

Начнём с того, что обновим списки доступных пакетов, а также обновим уже установленные пакеты (которые идут сразу с ОС). Доустанавливаем `git` и `screen`:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install git
sudo apt-get install screen
```

Установка Python'a и необходимой библиотеки `RPi.GPIO`, с помощью которой осуществляется управление пинами (штырьки, торчащие из RPi):
```
sudo apt-get install python-pip python3-pip python-dev python-rpi.gpio
pip3 install RPi.GPIO
```

Для `homebridge` и установки плагинов нам потребутеся nodejs, который установим следующими командами:
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```

На данном этапе стоит проверить тип чипа у RPi. Если это "armv7l", то всё ок, идём дальше:
```
uname -a
```

Устанавливаем `homebridge`:
```
sudo apt-get install libavahi-compat-libdnssd-dev
sudo npm install -g --unsafe-perm homebridge
```

Проверим, что всё установилось как надо. Для этого надо запустить команду `homebridge`:
![alt](/assets/images/homebridge.jpg){: .align-center}

**На всякий случай!** Если на каком-то этапе возникли трудности, то стоит поискать информацию в [репозитории `homebridge`](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi), [посмотреть хороший туториал](https://www.youtube.com/watch?v=g4Smfn1Q5Qc) по установке `homebridge`, либо же написать мне удобным для тебя способом.
{: .notice--warning}

### Установка Плагинов для homebridge

Плагины очень сильно упрощают подключения внешних устройств (таких как термостаты, реле, лампочки, датчики температуры, etc.). Все доступные плагины искать можно [здесь](https://www.npmjs.com/search?q=homebridge-plugin).

Разберём пару тех, которые я использую.

[**CmdSwitch2**](https://www.npmjs.com/package/homebridge-cmdswitch2) -- предоставляет интерфейс для управления выключателем (я его использую для управления реле).

[**homebridge-temperature-file**](https://github.com/bahlo/homebridge-temperature-file) -- удобный плагин для вывода температуры из файла в приложение `Home`.

```
sudo npm install -g homebridge-temperature-file
sudo npm install -g homebridge-cmdswitch2
```

### Запуск сервера homebridge при включении RPi (on boot)

1. Об этом написано подробно в [репозитории `homebridge`](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen)
2. Понадобится программа [`screen`](https://help.ubuntu.ru/wiki/screen):
```
sudo apt-get install screen
```
3. Запустить последовательность команд в фоне:
```
screen -dmS <screen_name> bash -c “<command1>; <command2>; <command3>;”
```
4. Запустить команду в фоне:
```
screen -dmS <screen_name> “<command>”
```
5. Закрыть запущенную программу в окне <screen_name>:
```
screen -S <screen_name> -X quit
```

### Adding lines to /etc/rc.local file

TODO

Проверка статуса сервиса. Тут должно отразиться, что мы действительно внесли изменения в файл `/etc/rc.local`:
```
sudo systemctl status rc-local
```

После этого перезапускаем сервис `rc-local`:
```
sudo systemctl daemon-reload
```

---

Буду рад услышать пожелания/предложения/замечания от тебя. Если что -- напиши мне :)
{: .notice--success}
