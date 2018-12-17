---
title: Проекты
permalink: "/projects/"
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.5'
  overlay_image: "/assets/images/projects/header.jpg"
  actions:
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  - label: GitHub
    url: https://github.com/akarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: На этой странице я соберу свои проекты (в основном с использованием Raspberry Pi и Arduino).

demoqst:
- image_path: assets/images/projects/demo_qst.jpg
  title: "Демонстрация томографии квантового состояния"
  excerpt: "Использовал светодиоды, шаговый двигатель, Raspberry Pi и фигурку \"нолик/единичка\", которую мне подарили из IBM"
  url: "/demo_qst/"
  btn_label: Read More
  btn_class: btn--primary

qkeypad:
- image_path: assets/images/projects/quantum_keypad.jpg
  title: "Квантовый Кейпад"
  excerpt: "Китайский кейпад и Raspberry Pi Zero W. Вдохновился идеей [Model Q](https://qiskit.org/modelq/), которую в качестве первоапрельской шутки в 2018 году представил QISKit (подразделение IBM, занимающееся разработкой квантового компьютера). Из IBM мне прислали различные подарки, когда увидели мой [пост в Twitter'e](https://twitter.com/antonkarazeev/status/981671571319336960)"
  url: "/proj_quantum_keypad/"
  btn_label: Read More
  btn_class: btn--primary

cameraslider:
- image_path: assets/images/projects/camera_slider.jpg
  title: "Слайдер для камеры"
  excerpt: "Это один из моих первых проектов, в которых я использовал Raspberry Pi. После покупки всех необходимых деталей я принялся сверлить и крутить винты. Получилось довольно прикольно (по ссылке есть 2 видео -- демонстрация работы и снятый таймлепс)"
  url: "/proj_camera_slider/"
  btn_label: Read More
  btn_class: btn--primary

joystick:
- image_path: assets/images/projects/joystick.jpg
  title: "Джойстик"
  excerpt: "Самодельный джойстик с использованием Raspberry Pi, датчика воды и аналогового стика"
  url: "/proj_joystick/"
  btn_label: Read More
  btn_class: btn--primary

homeautomation:
- image_path: assets/images/projects/homeautomation.jpg
  title: "Автоматизация домашних устройств. Raspberry Pi и Homekit"
  excerpt: "HomeKit это инициатива от Apple, направленная на распространение такого понятия как \"умный дом\" (дом умнее не становится, лишь что-то можно автоматизировать). На данный момент я автоматизировал освещение вокруг моего рабочего места. Есть [туториал](/home-automation-homekit/) по настройке сервера homebridge на Raspberry Pi"
  url: "/proj_homeautomation/"
  btn_label: Read More
  btn_class: btn--primary
---

{% include feature_row id="demoqst" type="left" %}

{% include feature_row id="qkeypad" type="right" %}

{% include feature_row id="cameraslider" type="left" %}

{% include feature_row id="joystick" type="right" %}

{% include feature_row id="homeautomation" type="left" %}
