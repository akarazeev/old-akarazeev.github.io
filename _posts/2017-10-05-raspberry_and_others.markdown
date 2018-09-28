---
title: Raspberry Pi + AirPlay + AirPrint + Telegram Chatbots + Apple HomeKit
date: 2017-10-05 00:00:00 +03:00
tags:
- Raspberry Pi
- AirPlay
- AirPrint
- HomeKit
- Telegram
- Chatbot
- Git
- Python
layout: post
header:
  image: "/assets/images/raspberry_and_others.jpg"
  teaser: "/assets/images/raspberry_and_others.jpg"
---

Если не оч дружишь с питоном и есть желание это исправить -> [https://vk.com/pythontutor](https://vk.com/pythontutor)

Надеюсь, для кого-то это послужит пинком в знакомстве с raspberry и натолкнёт на мысли/идеи по автоматизации чего-то у себя дома/на даче/работе/etc.

Хочу показать изи настройку на Raspberry **AirPrint-/AirPlay-/HomeKit**-серверов, а также запуск **Telegram**’овского бота.

План-капкан:
1. Купить Raspberry можно, например, [здесь](https://ru.aliexpress.com/item/RS-Version-2016-New-Raspberry-Pi-3-Model-B-Board-1GB-LPDDR2-BCM2837-Quad-Core-Ras/32789942633.html?spm=a2g0v.search0104.3.2.cmDDaK&ws_ab_test=searchweb0_0,searchweb201602_2_10152_10065_10151_10068_10344_5560015_10342_10343_10340_10341_10307_10301_10060_10155_10154_10056_10055_10054_5370015_10059_10534_10533_10532_100031_10099_10338_10339_5580015_10103_10102_10169_10052_10053_10107_10050_10142_10051_10084_10083_10080_10082_10081_10110_5590015_10111_10112_10113_10114_143_10312_10314_5570015_10078_10079_10211_10128_10073_10129_10125,searchweb201603_1,ppcSwitch_5&btsid=62955025-32ab-4f85-b40d-250afe491920&algo_expid=462b1142-f34e-47b3-b1e8-b2c9128888d9-0&algo_pvid=462b1142-f34e-47b3-b1e8-b2c9128888d9). Плюс третьей модели в том, что у неё Wi-Fi и Bluetooth есть встроенные (не надо отдельно покупать, а для моей второй модели пришлось)
2. Понадобится карточка MicroSD (у меня на 8 GB, хватает)
3. Качаем Raspbian [отсюда](https://www.raspberrypi.org/downloads/raspbian/) и [делаем](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) загрузочную флешку
4. Вставляем загрузочную флешку в Raspberry, подключаем мышку/клавиатуру/монитор и погнали

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/cobbler_view.jpg)

Добавлю, что с “Т-образной штукой” намного удобнее подключать радиодетали к Raspberry - мелким шрифтом нанесена нумерация и названия пинов.

На али: [“Т-образная штука”](https://ru.aliexpress.com/item/Free-shipping-Raspberry-Pi-model-B-plus-T-cobbler-expansion-DIY-kit-GPIO-cable-breadboard-GPIO/2035640647.html?shortkey=aaqUfq6n&addresstype=600), [реле](https://ru.aliexpress.com/item/5V-Relay-Module-1-Channel-Low-level-for-SCM-Household-Appliance-Control-For-Arduino/32555959741.html?spm=a2g0s.9042311.0.0.UkNt6y), [провода_1](https://ru.aliexpress.com/item/40pcs-20cm-2-54mm-1p-1p-Pin-Female-to-Female-Color-Breadboard-Cable-Jump-Wire-Jumper/1728848121.html?spm=a2g0s.9042311.0.0.BkJWjY), [провода_2](https://ru.aliexpress.com/item/Free-Shipping-40pcs-dupont-cable-jumper-wire-dupont-line-Male-to-Male-dupont-line-20cm-1P/32687696479.html?spm=a2g0v.10010108.1000013.6.11473adb0oTRcd&traffic_analysisId=recommend_2088_3_90158_iswistore&scm=1007.13339.90158.0&pvid=b829046b-ace2-4103-8bfa-207f02c7e27b&tpp=1)

## AirPrint

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/airprint.jpg)

1. Точно потребуется установить `git`:
    * `sudo apt-get install git`
2. Другие “недостающие пакеты” пакеты так же устанавливаются:
    * `sudo apt-get install <package_name>`
3. Необходимо получить файлик `.service`, чтобы Avahi научить работать с принтером. Для этого скачаем репозиторий со скриптом. Например, можно завести working directory: `~/WD`, а в ней `cloned_git`. Тогда внутри `~/WD/cloned_git` качаем репозиторий:
    * `git clone https://github.com/tjfontaine/airprint-generate`
4. Внутри `airprint-generate` запускаем:
    * `python2 airprint-generate.py -d /etc/avahi/services`
5. Перезапускаем Avahi:
    * `sudo service avahi-daemon restart`
6. Должно заработать - можно теперь искать “расшаренный принтер”. Если вылетают баги какие-то или принтер печатать отказывается (у меня было такое) - пиши мне -> [сюда_1](http://t.me/akarazeev), [сюда_2](http://vk.com/akarazeev), [сюда_3](mailto:anton.karazeev@gmail.com)

## AirPlay

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/airplay.jpg)

Вот [здесь](https://pimylifeup.com/raspberry-pi-airplay-receiver/) отличный гайд, выполняешь все 8 пунктов и всё работает.

## HomeKit

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/homekit.jpg)

Делал по [этому](http://home-smart-home.ru/homebridge-raspberry-pi-kak-nauchit-siri-matu/) гайду.
Если что-то не оч понятно - пиши мне -> [сюда_1](http://t.me/akarazeev), [сюда_2](http://vk.com/akarazeev), [сюда_3](mailto:anton.karazeev@gmail.com)

## Telegram Bot

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/telegrambot.jpg)

1. Качаем репозиторий:
    * `git clone https://github.com/akarazeevprojects/TelegramBot`
2. Переходим в `TelegramBot/`
3. Переключаемся на ветку `lamp`:
    * `git checkout lamp`
4. Теперь осталось добавить token нашего бота
5. Идем к [@BotFather](http://t.me/BotFather) и создаем нового бота через `/newbot`
6. Полученный токен записываем в файл `token.json`, находясь в `TelegramBot/`:
    * `vim token.json`
    * нажимаем `i`
    * вставляем такую строчку: `{"token": "<tkn>"}`, где `<tkn>` - скопированный токен
    * нажимаем `ESC`
    * теперь `Shift+ж` и затем `wq` - должно получиться `:wq`
    * затем `Enter`
    * примерно так выглядит содержимое `token.json`:
    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/token_json.jpg)
7. Фух, теперь можно запускать бота. На самом деле еще надо поставить недостающие модули - например, `pip install python-telegram-bot` и тому подобное, но это уже мелочи :)
    * `python bot.py`
    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/run_botpy.jpg)
8. Командой `/switch` в самом боте можно включить/выключить реле, а командой `/temp` узнать температуру процессора Raspberry
9. Про подключение реле - в коде управление идёт пином под номером 26
    * соответственно проводами соединить надо “IN” <-> GPIO26, “VCC” <-> “3V3”, “GND” <-> “GND”
    ![alt]({{ site.url }}{{ site.baseurl }}/assets/images/cobbler_view_top.jpg)

====================================================================

Классный туториал по системе git -> https://githowto.com/ru

Скопипастил из своего `~/.bash_aliases`:

```bash
# git-commands aliases
alias gs='git status'
alias gA='git add -A'
alias ga='git add'
alias gc='git commit -m'
alias gpm='git push origin master'
alias gph='git push origin HEAD'
alias gpo='git push origin'
alias gb='git branch'
alias gl='git log'
alias gch='git checkout'
alias gv='git remote -v'
alias gr='git reset'
alias gig='vim .gitignore'
```

Поместить в файл `~/.bashrc` строки, если отсутствуют:

```bash
if [ -f ~/.bash_aliases ]; then
	. ~/.bash_aliases
fi
```

Это туда же можно поместить:

```bash
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\[\033[1;93m\]\u@\h:\w -\[\033[00;32m\]\$(parse_git_branch)\[\033[00m\] $ "
```

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/branch_name.jpg)

Переменная `PS1` отвечает за `prompt`, а функция `parse_git_branch()` добавляет к `prompt`’у название бранча (ветки), если текущая директория - репозиторий.

Последовательность действий:
1. `gs` - проверка статуса репозитория (есть ли изменения изменения)
2. (a) `gA` - добавить все изменения в папке в коммит, (b) `ga <file_name>` - добавить изменение конкретного файла `<file_name>`
3. `gc '<message>'` - добавить сообщение к коммиту
4. (a) `gpm` - отправить изменения на сервер в `master`-ветку, (b) `gph` - отправить изменения на сервер в текущую ветку
