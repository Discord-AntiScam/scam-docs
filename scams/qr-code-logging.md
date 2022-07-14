---
permalink: scams/qr-code-logging
title: QR Code Logging
description: QR code logging is the act of grabbing someone's token through a QR code.
redirect_from:
- scams/methods/QR%20%Code%20Logging
- scams/methods/QR%20%Code%20Logging/ 
---
# QR Code Logging
- [General Summary](#general-summary)
- [History](#history)
- [How It Works](#how-it-works)

## General Summary
**QR code logging** is the act of grabbing someone's token through a QR code. Today, it is used most commonly with a disguise of fake verification.

## History
The Discord QR Code feature was added around December 2019, but it was already being used for malicious purposes a year later. Many people were spreading awareness on the Discord Help Center with posts like [this one](https://support.discord.com/hc/en-us/community/posts/360056292492-QR-Code-Scams-and-how-to-prevent-them). 

In May 2021, a developer by the name of [9P9](https://github.com/9P9) (known for creating token loggers) created the first "*QR code token logger*" that is still available on GitHub. Inititally the scam was for Discord Nitro, but in May 2022, the scam became more mainstream as it evolved into a fake verification scam involving various Discord bots such as [Wick](https://wickbot.com) and [Captcha.bot](https://captcha.bot). As this was new to many users, over 20,000 were scammed in one server (figure from total boost count) - and there's plenty more to add on.

## How It Works
> DO NOT PERFORM THIS ON ANYONE OTHER THAN YOURSELF.

A web request is sent to the Discord Remote Auth WebSocket `(wss://remote-auth-gateway.discord.gg/?v=1)` with an `Origin` header of `discord.com` (this allows it to spoof itself as the Discord website). Then once a request is sent, Discord gives the scraper a fingerprint, with the fingerprint it can now monitor the Discord QR Code, the scraper turns the fingerprint into a URL `(https://discordapp.com/ra/{fingerprint})`. This is how the URL that the QR Code uses, now the Discord scraper is monitoring the WebSocket, and once it recieves the `pending_finish` request (this is when you scan it). It returns the user data not including the token, but when it gets the `finish` request it now has your token.
