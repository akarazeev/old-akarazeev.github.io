---
title: Art
permalink: "/art-en/"
lang: en
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
  caption: "Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)"
excerpt: "Gallery of photos, videos and different things I call \"art\""

oshten:
- image_path: assets/images/art/1.png
  title: "Trip to Oshten"
  excerpt: "Travelled with my friend. Slept right in front of Oshten mountain"
  url: ""
  btn_label: TODO
  btn_class: btn--success

demoqst:
- image_path: assets/images/art/demo_qst.jpg
  title: "Demonstration of quantum state tomography"
  excerpt: "Used LEDs, stepper motor, Raspberry Pi and \"zero/one\" that was given to me by IBM"
  url: "/demo-qst-en/"
  btn_label: Read More
  btn_class: btn--primary

equipment:
- image_path: assets/images/art/equipment.jpg
  title: "Equipment"
  excerpt: ""
  url: ""
  btn_label: TODO
  btn_class: btn--primary

krepostnaya:
- image_path: assets/images/art/krepostnaya.jpg
  title: "Krepostnaya"
  excerpt: ""
  url: ""
  btn_label: TODO
  btn_class: btn--primary

qkeypad:
- image_path: assets/images/art/quantum_keypad.jpg
  title: "Quantum Keypad"
  excerpt: "Keypad and Raspberry Pi Zero W. I was inspired by [Model Q](https://qiskit.org/modelq/) that was presented as a joke on April Fool's day in 2018 by QISKit (department of IBM which develops quantum computers). IBM sent me different cool things when they saw this quantum keypad in my [post on Twitter](https://twitter.com/antonkarazeev/status/981671571319336960)"
  url: "/proj-quantum-keypad-en/"
  btn_label: Read More
  btn_class: btn--primary

winery:
- image_path: https://img.youtube.com/vi/3a75neNaW6c/0.jpg
  title: "Winery"
  excerpt: "Fall 2018 we finally visited this place and made a few shots with our drones under the warm rays of the Sun"
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
  title: "Time-lapse 2014. Krepostnaya"
  excerpt: "One of my first time-lapses in Krepostnaya"
  url: "https://youtu.be/hiuO7wAwjFY"
  btn_label: Watch on YouTube
  btn_class: btn--danger

outro:
- excerpt: "In case you want to follow my updates or consider somehow support me, there are such possibilities --&nbsp;[<i class=\"fab fa-twitter\"></i> @antonkarazeev](https://twitter.com/antonkarazeev){: .btn .btn--twitter} and [<i class=\"fab fa-paypal\"></i> Support](https://www.paypal.me/akarazeev){: .btn .btn--success}"
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
