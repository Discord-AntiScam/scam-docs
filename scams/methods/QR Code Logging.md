# QR Code Logging

- [General Summary](#general-summary)
- [History](#history)
- [How It Works](#how-it-works)

## General Summary

**QR Code Logging** is the act of grabbing someone's Discord token through a QR Code. Inititally the scam was for Discord Nitro, but it later evolved into a verification scam involving various Discord bots such as [Wick](https://wickbot.com) and [Captcha.bot](https://captcha.bot).

## History

The Discord QR Code feature was added around December 2019, but just the next year it was already being used for malicious purposes. In 2020 many people were spreading awareness on the Discord Help Center including posts such as [this](https://support.discord.com/hc/en-us/community/posts/360056292492-QR-Code-Scams-and-how-to-prevent-them). In May 2021, a developer by the name of [9P9](https://github.com/9P9) (known for creating token loggers) created the first "*QR Code Token Logger*" that is still avaliable on GitHub. After a while the QR Code Logging trend fell, but recently in May 2022 the scam came back in the form of a verification, as this was new to many users over 20,000 Discord messages were sent unauthoried by the user.

## How It Works

> DO NOT TRY ANYTHING MENTIONED TO ANYONE OTHER THAN YOURSELF.

A web request is sent to the Discord Remote Auth WebSocket `(wss://remote-auth-gateway.discord.gg/?v=1)` with an `Origin` header of `discord.com` (this allows it to spoof itself as the Discord website). Then once a request is sent, Discord gives the scraper a fingerprint, with the fingerprint it can now monitor the Discord QR Code, the scraper turns the fingerprint into a URL `(https://discordapp.com/ra/{fingerprint})`. This is how the URL that the QR Code uses, now the Discord scraper is monitoring the WebSocket, and once it recieves the `pending_finish` request (this is when you scan it). It returns the user data not including the token, but when it gets the `finish` request it now has your token.
