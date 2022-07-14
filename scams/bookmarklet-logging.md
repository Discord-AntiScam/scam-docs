---
permalink: scams/bookmarklet-logging
title: Bookmarklet Logging
description: **Bookmarklet logging** is the act of grabbing someone's token through a bookmark.
redirect_from:
- scams/methods/Bookmarklet%20Logging
- scams/methods/Bookmarklet%20Logging/
---
# Bookmarklet Logging
- [General Summary](#general-summary)
- [History](#history)
- [How It Works](#how-it-works)

## General Summary
**Bookmarklet logging** is the act of grabbing someone's token through a bookmark. Today, it is used most commonly with a disguise of fake verification.

## History
In 1992, [ViolaWWW](http://viola.org/) was released - just two years after [WorldWideWeb](https://www.w3.org/People/Berners-Lee/WorldWideWeb.html), the first ever internet browser. It was the first ever browser to have functionality like scripting, stylesheets, and more - among those mentioned, those ideas are still used to this day. More importantly, it introduced bookmarks.

After learning about ViolaWWW, two programmers - Marc Andreessen and Eric Bina - were inspired to create [Mosaic](http://www.ncsa.illinois.edu/enabling/mosaic), which was released in 1993. Mosaic also implemented bookmarks, and various other features that, alongside ViolaWWW's various other faults, made it the leading browser that threw the internet into mainstream territory.

Mosaic's team - now working on, called, and better known as Netscape - created LiveScript in 1995 after realizing that web developers and users alike wanted more dynamic pages that could be interacted with-- something that made Java blow up in popularity quickly. It was renamed to JavaScript before releasing with Netscape Navigator 2.0.

More importantly, in Netscape Navigator 4.0, Netscape added the ability to [run JavaScript from the personal toolbar](https://web.archive.org/web/20020611183734/http://developer.netscape.com/docs/manuals/communicator/jsguide/misc.htm#1005712) (the personal toolbar being the equivalent of the bookmarks bar we know today). This spawned [bookmarklets](http://www.bookmarklets.com/about/), which lets you run short helpful tools made up of JavaScript from your bookmarks bar. At the time, Netscape bookmarks were limited to 1,848 characters ([source](https://www.squarefree.com/bookmarklets/limits.html)), a limit that could be filled up very quickly - nowadays, there is no limit to the size of a bookmark URL besides what your computer can handle.

The earliest bookmarklet we can find that logs and reports your Discord token is December 2021. They recently began being used as a scam in the form of fake verification - the earliest we know of is May 2022.

## How It Works
> DO NOT PERFORM THIS ON ANYONE OTHER THAN YOURSELF.

When you login with Discord, a "token" is created which acts as something that authorizes you - similar to how bots use tokens. It is also what keeps you logged into your account.

The bookmarklet will obtain this token from your browser's [local storage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) and send it somewhere - usually to a [webhook](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) or a [web server](https://en.wikipedia.org/wiki/Web_server) they've set up. They can use that token to login to your account by changing *their* browser's local storage to match your token.
