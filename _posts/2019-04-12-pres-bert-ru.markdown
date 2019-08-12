---
title: BERT - Pre-training of Deep Bidirectional Transformers for Language Understanding
lang: ru
ref: presbert190412
date: 2019-04-12 03:00:01 +03:00
tags:
- NLP
- BERT
- Text Mining
- Extraction
- Presentation🎯
layout: post
header:
  teaser: "/images/bert.jpg"
---

![image-center]({{ page.header.teaser }}){: .align-center}

[Presentation]({{ site.url }}{{ site.baseurl }}/files/presentations/bert.pdf)

Firstly I’d like to tell you about general problems of Natural Language Processing like Language Modelling, Sentence Classification, etc. Then I’ll move to newly proposed model called BERT and give an overview about its improvement in many Natural Language Processing tasks. In the end I’ll briefly summarise all my talk.

So let’s start with the first part of my presentation. What are you thinking about when you hear Natural Language Processing? Actually it’s a field of research when person tries to train a machine understand human’s speech and do what it’s asked to do. For example you ask your phone to ask a pizza only by saying “I want large margarita”. And the system will do everything that is necessary to order a pizza in a nearest restaurant. I want to start with a more detailed example of basic Natural Language Processing task like Spam Classification. Imagine you have an inbox and you need to delete all the spam messages that you’re receiving. As you can see on the slide the model (in current case it’s BERT) builds an embedding of each email’s text (digital representation) and after that the classifier tries to predict whether it’s spam or just regular message from your friend. The main part here is of course building of precise embedding what the BERT is responsible for.

Now let’s move to second part of my talk which is finally about the proposed BERT model. Researchers from Google reported that it took about 4 days to train such a model using cutting edge hardware called Tensor Processor Units which were designed specifically for such tasks. The amount of training data was huge. But the result is definitely worth it — I’ll talk about it a bit later. As I mentioned earlier with BERT they achieved state of the art result in many Natural Language Processing tasks such as Language Modeling, Named Entity Recognition, and so on. There are two models of BERT — a small and a big one with 12 and 24 layers correspondingly.

That brings me to the final part of my presentation. Here I want to show the result that were achieved with BERT. As you can see proposed model has beaten all the high scores of all the tasks.

I hope my presentation wasn’t too boring for you. As a conclusion I want to say that proposed and trained model is a huge improvement in the field of Natural Language Processing. It makes the future in which people and robots can freely interact with each other much closer to nowadays.
