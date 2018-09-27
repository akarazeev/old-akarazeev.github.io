---
title: Пишем простого Телеграм-бота
date: 2018-09-21 18:00:00 +03:00
tags:
- Telegram
- Bot
- Chatbot
- Tutorial
layout: single
---

![image-center](/assets/images/telegrambot.jpg){: .align-center}

Примерный план:
{: .text-center}

1. Склонировать репозиторий [`TinyTelegramBot`](https://github.com/akarazeevprojects/TinyTelegramBot), в котором лежат необходимые файлы:
```
git clone https://github.com/akarazeevprojects/TinyTelegramBot
```
2. Определиться с его названием (придумать username) -> с помощью специального бота [`@BotFather`](https://t.me/BotFather) получить токен для твоего бота (для идентификации его в системе Телеграм)
3. Реализовать бота. Представленный здесь код будет написан на Python'e и с использованием библиотеки [`python-telegram-bot`](https://github.com/python-telegram-bot/python-telegram-bot)
4. Поднять `socks-proxy` сервер на порте `9050` (получится адрес `127.0.0.1:9050`)

## Получение токена

Просим [`@BotFather`](https://t.me/BotFather) создать нового бота, сообщаем название/username/etc. -> получаем токен. Токен имеет следующий вид:
```
111111111:AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
```

Теперь его необходимо поместить в файл `EMPTY_TOKEN.json` вместо `<YOUR_TOKEN>`.

Переименовываем файл `EMPTY_TOKEN.json` -> `token.json`.

**На всякий случай!** Все указанные здесь файлы из репозитория [`TinyTelegramBot`](https://github.com/akarazeevprojects/TinyTelegramBot). Его надо было скачать первым делом.
{: .notice--warning}

## Бот. Реализация

Если на твоей машине не стоит питоновская библиотека `python-telegram-bot`, то её необходимо поставить с помощью команды
```
pip install python-telegram-bot --upgrade
```
(для справки: [`python-telegram-bot`](https://github.com/python-telegram-bot/python-telegram-bot)).

Вдаваться в подробности каждого объекта не будем, объясню основные моменты.

### Начнём с метода .add_handler() — добавление хэндлеров

Внутри файла `main.py` есть такие строчки:

{% highlight python linenos %}
dp.add_handler(CommandHandler('start', start))
dp.add_handler(CommandHandler('help', help))
dp.add_handler(MessageHandler(Filters.text, response))
{% endhighlight %}

Хэндлер — метод, который будет вызван в ответ на какую-то команду, либо же тип сообщения — как на третьей строчке.

Первыми двумя строчками задаётся действие бота на команды `/start` и `/help` соответственно (в кавычках название команды).

Например,

```python
CommandHandler('command_title', process_something)
```

означает, что по команде `/command_title` будет вызываться функция `process_something()`.

Рассмотрим простую функцию `start()`, которая выступает в качестве хэндлера для команды `/start`:

{% highlight python linenos %}
def start(bot, update):
    update.message.reply_text(start_text)
    return
{% endhighlight %}

Аргументы `bot` и `update` должны присутствовать. Из `update` можно получить текст сообщения пользователя, `id` пользователя и многое другое.

Эта функция `start()` всего лишь отправляет текст `start_text` в ответ на вызов команды `/start`.

**На всякий случай!** Все указанные здесь файлы из репозитория [`TinyTelegramBot`](https://github.com/akarazeevprojects/TinyTelegramBot). Его надо было скачать первым делом.
{: .notice--warning}

## Осталось поднять proxy на порте `9050`

Думаю, ты справишься с этим :) Просто погугли "install proxy 9050" или что-то в таком духе.

## Запуск

Для запуска бота необходимо выполнить `python main.py`. Если высветилось "-> USE PROXY", то всё ок — можно слать сообщения боту.

***

Ввиду того, что я редко пишу подобные длинные посты, читать их будет определённо не так же кайфово как какую-нибудь художественную литературу. Сорян, я работаю над собой в этом направлении и надеюсь, что результаты станут скоро заметны.

А на этот раз всё, буду рад услышать комментарии/пожелания/замечания/... от тебя — для связи со мной можешь использовать любой удобный способ, перечисленный в моих контактах. Но лучше — писать в телеге [@akarazeev](https://t.me/akarazeev) :smirk:
