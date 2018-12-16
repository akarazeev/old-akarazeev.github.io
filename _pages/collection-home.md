---
title: "Anton Karazeev"
permalink: "/"
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.5'
  overlay_image: "/assets/images/home/header.jpg"
  actions:
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  - label: GitHub
    url: https://github.com/akarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: "Привет! Раз ты здесь, то наверное тебя заинтересовало какое-то из моих видео на youtube, какой-то из моих проектов на гитхабе... а может и нет"

intro:
- excerpt:  "На этом сайте я попытаюсь навести порядок и как-то структурировать свои идеи/проекты/etc. Возможно, тебе будет интереснее просто посетить мои профили -- [YouTube](http://youtube.com/c/AntonKarazeev), [Instagram](https://instagram.com/akarazeev), [GitHub](https://github.com/akarazeev)"

hacks:
- image_path: "/assets/images/home/junction2017.jpg"
  title: "Хакатоны (Hackathons)"
  excerpt: "В 2016 году я впервые участвовал в хакатоне. Он назывался Junction 2016 и проходил в столице Финляндии -- Хельсинки. С тех пор я участвовал в 10+ хакатонах.


Мне нравится атмосфера, работа в команде и тот факт, что за короткий промежуток времени (обычно это 2 дня), мы делаем что-то \"новое и прикольное\""
  url: "/junction-2016/"
  btn_label: Junction 2016
  btn_class: btn--warning

diy:
- image_path: "/assets/images/home/quantum_keypad.jpg"
  title: "Проекты Internet of Things (IoT) и Do It Yourself (DIY)"
  excerpt: "Позволь мне начать с моих проектов, в которых я часто использую Raspberry Pi, Arduino и различные вспомогательные модули. Благодаря этому увлечению я научился паять, работать с проводами и пр."
  url: "/projects/"
  btn_label: Projects
  btn_class: btn--success

ml:
- image_path: "/assets/images/home/medium.jpg"
  title: "{Machine, Deep, Reinforcement} Learning"
  excerpt: "Проектов по ML у меня не так много. Зато есть статья на платформе Medium про GAN'ы. Когда-то я был на втором месте сразу за Goodfellow (создатель GAN'ов) на платформе Quora по количеству просмотров в теме Generative Adversarial Networks (GANs)"
  url: "https://blog.statsbot.co/generative-adversarial-networks-gans-engine-and-applications-f96291965b47"
  btn_label: Medium
  btn_class: btn--info

photos:
- title: "Фото и видео"
  excerpt: "Я очень люблю обрабатывать видео, которые в последние месяцы я стал часто снимать. До этого я фотографировал и любил засесть на какое-то время за обработку фотографий в Lightroom'e


Хожу в лес и горы. Там заниматься съёмкой мне нравится больше всего. Тем более помехи минимальны -- это важно при съёмке дроном


Ввиду того, что мой дрон, DJI Spark, довольно маленький и передатчиктам не самый сильный, в городе у меня пропадает связь между пультом и дроном. Не очень приятно. А вот в горах и лесах ситуация совсем другая"
- image_path: "/assets/images/home/banya.jpg"
  excerpt: "По этой ссылке \"Art\" я организую нечто вроде выставки из фотографий (\"оригиналов\" и ссылок на instagram) и видео (ссылки на youtube)"
  url: "/art/"
  btn_label: Art
  btn_class: btn--danger

paypal:
- image_path: "/assets/images/unsplash-gallery-image-2-th.jpg"
  alt: placeholder image 2
  title: Donate
  excerpt: TODO
  url: "#test-link"
  btn_label: Read More
  btn_class: btn--primary
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="diy" type="left" %}

{% include feature_row id="hacks" type="center" %}

{% include feature_row id="ml" type="right" %}

{% include feature_row id="photos" type="center" %}
