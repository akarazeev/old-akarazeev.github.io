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
  title: "Hackathons"
  excerpt: "In 2016 I attended the hackathon for the first time. It called Junction 2016 and was held in the capital of Finland -- Helsinki. Since then I've been participating in 10+ hackathons


I love the atmosphere, joint work with team mates and the fact that after a short period of time (usually 2 days) we create something new and cool"
  url: "/junction-2016-en/"
  btn_label: Junction 2016
  btn_class: btn--warning

diy:
- image_path: "/assets/images/about/quantum_keypad.jpg"
  title: "Internet of Things (IoT) and Do It Yourself (DIY) Projects"
  excerpt: "Let me begin the introduction with one of my favorite projects -- in which I often use Raspberry Pi, Arduino and different electronic components. Due to this hobby I've learned to solder, work with wires and so on"
  url: "/projects-en/"
  btn_label: Projects
  btn_class: btn--success

ml:
- image_path: "/assets/images/about/medium.jpg"
  title: "{Machine, Deep, Reinforcement} Learning"
  excerpt: "I don't have many projects related to ML. But I do have an article on Medium platform about Generative Adversarial Networks (GANs). Also I was at 2nd place (right behind the Ian Goodfellow) by the views of answers on Quora platform in GANs-related section (now I'm at 3rd place)"
  url: "https://blog.statsbot.co/generative-adversarial-networks-gans-engine-and-applications-f96291965b47"
  btn_label: Medium
  btn_class: btn--info

photos:
- title: "Photo and Video"
  excerpt: "I love video editing. During last months I've been shooting a lot, almost everywhere I go and travel. Used to I made photos and loved to edit them in Lightroom. I could do this for hours


Visit forests and mountains (trying to do it more often). I love to shoot there and shootings are more effortless there too due to the absence of interference -- it's important when you're flying with the drone


My drone (DJI Spark) is pretty small and its transmitter/receiver isn't strong enough. Especially when I'm in a city (where the connection between the drone and remote controller can be lost easily). In forests and mountains the situation is far different"
- image_path: "/assets/images/about/banya.jpg"
  excerpt: "This button \"Art\" will lead you to the place where I'll organize something similar to gallery of photos, videos and art of different kind that I've ever made. Hope you'll enjoy it"
  url: "/art-en/"
  btn_label: Art
  btn_class: btn--danger

outro:
- excerpt:  "Congratulations, now you know something about me. In case you want to follow my updates or consider somehow support me, there are such possibilities --&nbsp;[<i class=\"fab fa-twitter\"></i> @antonkarazeev](https://twitter.com/antonkarazeev){: .btn .btn--twitter} and [<i class=\"fab fa-paypal\"></i> Support](https://www.paypal.me/akarazeev){: .btn .btn--success}"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="diy" type="left" %}

{% include feature_row id="hacks" type="center" %}

{% include feature_row id="ml" type="right" %}

{% include feature_row id="photos" type="center" %}

{% include feature_row id="outro" type="center" %}
