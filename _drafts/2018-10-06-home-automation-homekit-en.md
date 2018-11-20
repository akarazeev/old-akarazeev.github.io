---
title: Home Automation with Raspberry Pi using HomeKit
date: 2018-10-06 06:00:00 +03:00
tags:
- Raspberry Pi
- Home Automation
- HomeKit
- Apple
layout: single
header:
  teaser: "/assets/images/rpi-homekit.png"
---

![image-center]({{ page.header.teaser }}){: .align-center}

First of all we need to install OS on our micro computer -- Raspberry Pi.

So I download an image from [https://www.raspberrypi.org/downloads/raspbian/](https://www.raspberrypi.org/downloads/raspbian/) with Transmission torrent application:

![alt](/assets/images/torrent.jpg)

Then we need to unzip this file and we receive `.img` file.

Using the Etcher app and with micro sd card inserted I will write the image of OS onto sd card.

![alt](/assets/images/etcher.jpg)
![alt](/assets/images/sdcard.jpg)

After the process has been completed I removed the card and inserted it into the Raspberry Pi. You need a keyboard and a monitor connected to initially set up Raspberry Pi.

After the set up I will connect to it with `ssh`.

To login for the first time you need to fill "pi" as `username` and "raspberry" as `password`.

### Setting Wi-Fi connection:

1. `sudo raspi-config`
2. "2. Network Options"
3. "N2. Wi-fi"
4. Choose your country
5. Enter the SSID (name) of your network
6. Enter the passphrase (password)
7. Press "Finish" button

Now your Raspberry Pi is connected to Wi-Fi. It can be checked with `ping google.com` -- 0% packet loss.


### SSH

1. `sudo raspi-config`
2. "5. Interfacing Options"
3. "P2. SSH"
4. "Yes"
5. "Ok"
6. Press "Finish" button

### Setting up homebridge

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install git
sudo apt-get install screen
```

```
sudo apt-get install python-pip python3-pip python-dev python-rpi.gpio
pip3 install RPi.GPIO
```

```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs

uname -a  # to determine which type of chip RPi has. My RPi2 has “armv7l”

sudo apt-get install libavahi-compat-libdnssd-dev

sudo npm install -g --unsafe-perm homebridge
```

![alt](/assets/images/homebridge.jpg)

### Adding lines to /etc/rc.local file
```
sudo systemctl status rc-local # check status of service
sudo systemctl daemon-reload # to apply changes
```

Check whether everything is fine with running `homebridge` command.

sudo npm install -g homebridge-temperature-file # https://github.com/bahlo/homebridge-temperature-file
sudo npm install -g homebridge-cmdswitch2 # https://www.npmjs.com/package/homebridge-cmdswitch2

### Start homebridge server on boot

1. https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi#running-homebridge-on-boot-etcrclocal-using-screen
2. Понадобится программа screen (https://help.ubuntu.ru/wiki/screen): `sudo apt-get install screen`
3. Запустить последовательность команд в фоне: `screen -dmS <screen_name> bash -c “<command1>; <command2>; <command3>;”`
4. Запустить команду в фоне: `screen -dmS <screen_name> “<command>”`
5. Закрыть запущенную программу в окне <screen_name>: `screen -S <screen_name> -X quit`

Great video tutorial https://www.youtube.com/watch?v=g4Smfn1Q5Qc
