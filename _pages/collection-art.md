---
title: Art
permalink: "/art/"
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: '0.5'
  overlay_image: "/assets/images/splash/header.jpg"
  actions:
  - label: GitHub
    url: https://github.com/akarazeev
  - label: Instagram
    url: https://instagram.com/akarazeev
  - label: YouTube
    url: http://youtube.com/c/AntonKarazeev
  caption: 'Photo credit: [**Anton Karazeev**](https://instagram.com/akarazeev)'
excerpt: Привет. Возможно, ты видел мои видосики на youtube или мои проекты на github'e. У меня есть ещё этот сайт, на котором вот уже который месяц я пытаюсь "навести порядок" и как-то структирировать свои идеи/проекты/...
intro:
- excerpt: Nullam suscipit et nam, tellus velit pellentesque at malesuada, enim eaque.
    Quis nulla, netus tempor in diam gravida tincidunt, *proin faucibus* voluptate
    felis id sollicitudin. Centered with `type="center"`
feature_row:
- image_path: assets/images/unsplash-gallery-image-1-th.jpg
  alt: placeholder image 1
  title: Placeholder 1
  excerpt: This is some sample content that goes here with **Markdown** formatting.
- image_path: "/assets/images/unsplash-gallery-image-2-th.jpg"
  image_caption: Image courtesy of [Unsplash](https://unsplash.com/)
  alt: placeholder image 2
  title: Placeholder 2
  excerpt: This is some sample content that goes here with **Markdown** formatting.
  url: "#test-link"
  btn_label: Read More
  btn_class: btn--primary
- image_path: "/assets/images/unsplash-gallery-image-3-th.jpg"
  title: Placeholder 3
  excerpt: This is some sample content that goes here with **Markdown** formatting.
feature_row2:
- image_path: "/assets/images/unsplash-gallery-image-2-th.jpg"
  alt: placeholder image 2
  title: Placeholder Image Left Aligned
  excerpt: This is some sample content that goes here with **Markdown** formatting.
    Left aligned with `type="left"`
  url: "#test-link"
  btn_label: Read More
  btn_class: btn--primary
feature_row3:
- image_path: "/assets/images/unsplash-gallery-image-2-th.jpg"
  alt: placeholder image 2
  title: Placeholder Image Right Aligned
  excerpt: This is some sample content that goes here with **Markdown** formatting.
    Right aligned with `type="right"`
  url: "#test-link"
  btn_label: Read More
  btn_class: btn--primary
feature_row4:
- image_path: "/assets/images/unsplash-gallery-image-2-th.jpg"
  alt: placeholder image 2
  title: Placeholder Image Center Aligned
  excerpt: This is some sample content that goes here with **Markdown** formatting.
    Centered with `type="center"`
  url: "#test-link"
  btn_label: Read More
  btn_class: btn--primary
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
