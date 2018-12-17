---
title: "Anton Karazeev"
permalink: "/en"
redirect_from: "/"
ref: about
lang: en

layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.3'
  overlay_image: "/assets/images/about/header.jpg"
  actions:
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  - label: GitHub
    url: https://github.com/akarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: "Hi! I'm glad to see you here. Suppose that you were interested with one of my videos on youtube, one of my projects on github... or probably not"

intro:
- excerpt:  "Here I'm trying to sort all the things that I've done (projects/ideas/etc.). Probably it's more interesting for you to visit my profiles -- [YouTube](http://youtube.com/c/AntonKarazeev), [Instagram](https://instagram.com/akarazeev), [GitHub](https://github.com/akarazeev)"

hacks:
- image_path: "/assets/images/about/junction2017.jpg"
  title: "Хакатоны (Hackathons)"
  excerpt: "В 2016 году я впервые участвовал в хакатоне. Он назывался Junction 2016 и проходил в столице Финляндии -- Хельсинки. С тех пор я участвовал в 10+ хакатонах.


Мне нравится атмосфера, работа в команде и тот факт, что за короткий промежуток времени (обычно это 2 дня), мы делаем что-то \"новое и прикольное\""
  url: "/junction-2016/"
  btn_label: Junction 2016
  btn_class: btn--warning

diy:
- image_path: "/assets/images/about/quantum_keypad.jpg"
  title: "Internet of Things (IoT) and Do It Yourself (DIY) Projects"
  excerpt: "Let me begin the introduction with one of my favorite projects -- in which I often use Raspberry Pi, Arduino and different electronic components. Due to this hobby I've learned to solder, work with wires and so on"
  url: "/projects/"
  btn_label: Projects
  btn_class: btn--success

ml:
- image_path: "/assets/images/about/medium.jpg"
  title: "{Machine, Deep, Reinforcement} Learning"
  excerpt: "Проектов по ML у меня не так много. Зато есть статья на платформе Medium про GAN'ы. Когда-то я был на втором месте сразу за Goodfellow (создатель GAN'ов) на платформе Quora по количеству просмотров в теме Generative Adversarial Networks (GANs)"
  url: "https://blog.statsbot.co/generative-adversarial-networks-gans-engine-and-applications-f96291965b47"
  btn_label: Medium
  btn_class: btn--info

photos:
- title: "Фото и видео"
  excerpt: "Я очень люблю обрабатывать видео, которые в последние месяцы я стал часто снимать. До этого я фотографировал и любил засесть на какое-то время за обработку фотографий в Lightroom'e


Хожу в лес и горы. Там заниматься съёмкой мне нравится больше всего. Тем более помехи минимальны -- это важно при съёмке дроном


Ввиду того, что мой дрон, DJI Spark, довольно маленький и передатчик там не самый сильный, в городе у меня пропадает связь между пультом и дроном. Не очень приятно. А вот в горах и лесах ситуация совсем другая"
- image_path: "/assets/images/about/banya.jpg"
  excerpt: "По этой ссылке \"Art\" я организую нечто вроде выставки из фотографий (\"оригиналов\" и ссылок на instagram) и видео (ссылки на youtube)"
  url: "/art/"
  btn_label: Art
  btn_class: btn--danger

outro:
- excerpt:  "Поздравляю, теперь у тебя есть представление обо мне. Если хочешь быть в курсе моих действий или есть желание меня поддержать, то такие возможности есть --&nbsp;[<i class=\"fab fa-twitter\"></i> @antonkarazeev](https://twitter.com/antonkarazeev){: .btn .btn--twitter} и [<i class=\"fab fa-paypal\"></i> Поддержать](https://www.paypal.me/akarazeev){: .btn .btn--success}"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="diy" type="left" %}

{% include feature_row id="hacks" type="center" %}

{% include feature_row id="ml" type="right" %}

{% include feature_row id="photos" type="center" %}

{% include feature_row id="outro" type="center" %}
