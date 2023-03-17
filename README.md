# Simple Python Telegram bot template

This repository contains all you may need to bootstrap your new Telegram bot in Python.
It makes use of the awesome [`python-telegram-bot`](https://github.com/python-telegram-bot/python-telegram-bot) library, 
and a [basic example](https://github.com/python-telegram-bot/python-telegram-bot/blob/master/examples/echobot.py) 
from the official repository.

## A `requirements.txt` file

This file contains all dependencies for the bot project.
For the template and the basic behaviour of the bot, only the package `python-telegram-bot` is needed.

You can just run this command in order to get dependencies installed:
```shell
pip install -r requirements.txt
```

🛑 **Note**: the version number for the package **is not being set**. This will cause downloading always the latest version 
of the package. If you don't want this behaviour, please modify the `requirements.txt` file to set it.
For example:
```text
python-telegram-bot==13.6
```

# Configuring your new bot

The only thing you need to get started with bots in Telegram is an account and to talk to 
[BotFather](https://t.me/BotFather). This bot will provide you instructions to create a new bot, and at the end will
provide you **a token**.

You will need this token and keep it secret (**don't ever commit it to GitHub or make it public in any way**).
Once you have this token, you can set it to the bot via an 
[environment variable](https://en.wikipedia.org/wiki/Environment_variable) or directly in code.

## Setting the token as an environment variable

If running your code directly from the terminal, declare the environment variable `TOKEN` with your token as its 
value.
For example, in Linux or macOS:
```shell
export TOKEN="mysupersecrettoken"
```

## Setting the token inside the code

Search in the `main.py` file for the `PUT_YOUR_TOKEN_HERE` word (it is in the `main` method).
As you can see, the program will attempt to load the token from an environment variable named `TOKEN`.
Nevertheless, if this environment variable does not exist, the second parameter will be used by default.

If you change that second parameter, the bot will get the correct token directly from the code 
(just ensure the is no environment variable named `TOKEN` created).
