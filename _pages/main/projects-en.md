---
title: Projects
permalink: "/projects-en/"
lang: en
ref: projects

layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.3'
  overlay_image: "/assets/images/projects/header.jpg"
  actions:
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  - label: GitHub
    url: https://github.com/akarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: My projects in which I usually use Raspberry Pi and Arduino

demoqst:
- image_path: assets/images/projects/demo_qst.jpg
  title: "Demonstration of Quantum State Tomography"
  excerpt: "Used LEDs, stepper motor, Raspberry Pi and \"zero/one\" that was given to me by IBM"
  url: "/demo-qst-en/"
  btn_label: Read More
  btn_class: btn--primary

qkeypad:
- image_path: assets/images/projects/quantum_keypad.jpg
  title: "Quantum Keypad"
  excerpt: "Keypad and Raspberry Pi Zero W. I was inspired by [Model Q](https://qiskit.org/modelq/) that was presented as a joke on April Fool's day in 2018 by QISKit (department of IBM which develops quantum computers). IBM sent me different cool things when they saw this quantum keypad in my [post on Twitter](https://twitter.com/antonkarazeev/status/981671571319336960)"
  url: "/proj-quantum-keypad-en/"
  btn_label: Read More
  btn_class: btn--primary

cameraslider:
- image_path: assets/images/projects/camera_slider.jpg
  title: "Camera Slider"
  excerpt: "It's one of my first projects with Raspberry Pi. After buying of necessary parts I started to drill and twist the screws. The result turned out to be pretty cool (the link will lead you to 2 videos -- demonstration of work and a time-lapse shot using my camera slider)"
  url: "/proj-camera-slider-en/"
  btn_label: Read More
  btn_class: btn--primary

joystick:
- image_path: assets/images/projects/joystick.jpg
  title: "Joystick"
  excerpt: "DIY joystick using Raspberry Pi, water-level sensor and analogue stick"
  url: "/proj-joystick-en/"
  btn_label: Read More
  btn_class: btn--primary

homeautomation:
- image_path: assets/images/projects/homeautomation.jpg
  title: "Home Automation with Raspberry Pi and Homekit"
  excerpt: "HomeKit is a toolkit by Apple that helps to turn any home into the \"smart home\" (actually, the home won't become \"smart\", rather some things will become automated, e.g. the lights). Currently I automated all the lights and fan around my work place. There are [tutorial](/home-automation-homekit-en/) on how to set up homebridge server on Raspberry Pi"
  url: "/proj-homeautomation-en/"
  btn_label: Read More
  btn_class: btn--primary

outro:
- excerpt: "In case you want to follow my updates or consider somehow support me, there are such possibilities --&nbsp;[<i class=\"fab fa-twitter\"></i> @antonkarazeev](https://twitter.com/antonkarazeev){: .btn .btn--twitter} and [<i class=\"fab fa-paypal\"></i> Support](https://www.paypal.me/akarazeev){: .btn .btn--success}"
---

{% include feature_row id="demoqst" type="left" %}

{% include feature_row id="qkeypad" type="right" %}

{% include feature_row id="cameraslider" type="left" %}

{% include feature_row id="joystick" type="right" %}

{% include feature_row id="homeautomation" type="left" %}

{% include feature_row id="outro" type="center" %}
