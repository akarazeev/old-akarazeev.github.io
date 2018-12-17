---
title: Art
permalink: "/art-ru/"
lang: ru
ref: art

layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.3'
  overlay_image: "/assets/images/art/header.jpg"
  actions:
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  - label: GitHub
    url: https://github.com/akarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: Галерея фотографий, видео и какого-нибудь ещё арта.

oshten:
- image_path: assets/images/art/1.png
  title: "Поход к Оштену"
  excerpt: "Ходили вместе с товарищем. Ночевали прямо у подножия Оштена"
  url: ""
  btn_label: TODO
  btn_class: btn--success

demoqst:
- image_path: assets/images/art/demo_qst.jpg
  title: "Демонстрация томографии квантового состояния"
  excerpt: "Использовал светодиоды, шаговый двигатель, Raspberry Pi и фигурку \"нолик/единичка\", которую мне подарили из IBM"
  url: "/demo_qst/"
  btn_label: Read More
  btn_class: btn--primary

equipment:
- image_path: assets/images/art/equipment.jpg
  title: "Аппаратура"
  excerpt: ""
  url: ""
  btn_label: TODO
  btn_class: btn--primary

krepostnaya:
- image_path: assets/images/art/krepostnaya.jpg
  title: "Крепостная"
  excerpt: ""
  url: ""
  btn_label: TODO
  btn_class: btn--primary

qkeypad:
- image_path: assets/images/art/quantum_keypad.jpg
  title: "Квантовый Кейпад"
  excerpt: "Китайский кейпад и Raspberry Pi Zero W. Вдохновился идеей [Model Q](https://qiskit.org/modelq/), которую в качестве первоапрельской шутки в 2018 году представил QISKit (подразделение IBM, занимающееся разработкой квантового компьютера). Из IBM мне прислали различные подарки, когда увидели мой [пост в Twitter'e](https://twitter.com/antonkarazeev/status/981671571319336960)"
  url: "/proj_quantum_keypad/"
  btn_label: Read More
  btn_class: btn--primary

winery:
- image_path: https://img.youtube.com/vi/3a75neNaW6c/0.jpg
  title: "Винодельня"
  excerpt: "Осенью 2018 наконец-то посетили это место и полетали на дронах в лучах тёплого солнца"
  url: "https://youtu.be/3a75neNaW6c"
  btn_label: Watch on YouTube
  btn_class: btn--danger

yolo2017:
- image_path: https://img.youtube.com/vi/VoPkj_x4108/0.jpg
  title: "YOLO 2017"
  excerpt: "..."
  url: "https://youtu.be/VoPkj_x4108"
  btn_label: Watch on YouTube
  btn_class: btn--danger

timelapse2014:
- image_path: https://img.youtube.com/vi/hiuO7wAwjFY/0.jpg
  title: "Таймлепс 2014. Крепостная"
  excerpt: "Один из первых моих таймлепсов, которые я снимал в Крепостной"
  url: "https://youtu.be/hiuO7wAwjFY"
  btn_label: Watch on YouTube
  btn_class: btn--danger

outro:
- excerpt: "Если хочешь быть в курсе моих действий или есть желание меня поддержать, то такие возможности есть --&nbsp;[<i class=\"fab fa-twitter\"></i> @antonkarazeev](https://twitter.com/antonkarazeev){: .btn .btn--twitter} и [<i class=\"fab fa-paypal\"></i> Поддержать](https://www.paypal.me/akarazeev){: .btn .btn--success}"
---

{% include feature_row id="oshten" type="left" %}

{% include feature_row id="timelapse2014" type="right" %}

{% include feature_row id="demoqst" type="left" %}

{% include feature_row id="krepostnaya" type="right" %}

{% include feature_row id="yolo2017" type="left" %}

{% include feature_row id="qkeypad" type="right" %}

{% include feature_row id="equipment" type="left" %}

{% include feature_row id="winery" type="right" %}

{% include feature_row id="outro" type="center" %}
