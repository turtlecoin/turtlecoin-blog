---
layout: "post"
title: "This Week In TurtleCoin (Feb 4, 2019)"
description: "I’ve managed to get the TurtleCoin binaries to compile on Alpine. There were a couple of issues that were preventing this. The first issue is that ucontext was deprecated in POSIX which musl adheres…"
image: "{{ site.baseurl }}/images/0FMgGQCdjXxAECkY9.jpg"
date: "2019-02-05T00:57:29.421Z"
---

![]({{ site.baseurl }}/images/0FMgGQCdjXxAECkY9.jpg)

![]({{ site.baseurl }}/images/0DIKnOs6L2XYZNcLw.jpg)

# Developer Updates

![]({{ site.baseurl }}/images/0Zz2U6A5gWdvtKeAN.png)

I’ve managed to get the TurtleCoin binaries to compile on Alpine. There were a couple of issues that were preventing this. The first issue is that ucontext was deprecated in POSIX which musl adheres to. Thankfully someone had created a library that solves the problem. The second issue was that musl has a PAGE_SIZE macro defined in limits.h that was conflicting with a parameter used on slow-hash.c. This has now been changed to page_size in the core, resolving the conflict. So far, I’ve created three images. The first image, which is meant to be a starting point for your own images, builds all the binaries in Alpine then copies them to a scratch container resulting in an image size of 22.6MB. The zedwallet container comes in at 7.96MB and the TurtleCoind image, which includes checkpoints, is only 90MB. I plan to create a series of docker-compose files that will tie them together to help accomplish various tasks. You can view the images on Docker Hub — Andrew | trtl.rocks

<https://hub.docker.com/r/andrewnk/turtlecoin> or on github: <https://github.com/andrewnk/turtlecoin-docker>

![]({{ site.baseurl }}/images/0HjP9QzvTyMjmQuTL.png)

**trtl-rocks —** I’ve made several improvements and changes to the website. I made a silly logic error that caused the initial load time to vary drastically or stall altogether. If the node or pool API is not accessible, then it won’t be shown on the site. If you don’t see your node or pool in the list, this is most likely the reason. I’ve cleaned up the line chart, including formatting y-axis and point labels, which should help readability. I’ve added tooltips to most table headers that describe what the column represents. These can be turned on or off by toggling the Tooltips switch on the bottom right hand of the screen. Finally, I’ve added the ability to switch the line chart between live and historical data. On initial load, the live mode will be enabled and updates are displayed whenever the data is pushed from the database. I’m in the process of rewriting iburn’s blockexplorer-cache library to use sequelize, which will help me move on to the block explorer portion of the site. **— Andrew | trtl.rocks**

[andrewnk/turtle-explorerContribute to andrewnk/turtle-explorer development by creating an account on GitHub.github.com](https://github.com/andrewnk/turtle-explorer)

**Turtle Simulator** has now been uploaded to GitHub! If you want to help with the project, or if you if you are interested in game design, check out the code and give me a message in #Dev_gaming channel! Im looking for anyone who knows: 3d Modeling/ Animation/ UV maps. Coding in UE4, Blueprints or C++ Music /Audio Ideas / Level design It’s a massive project I’ve undertaken so any help takes something off my to-do list. Thanks in advanced! Looking forward to see what we can make together! Oiboo P.s No minimum skill level, all help will be appreciated! — Oiboo

[Oiboo/TRTL-SimulatorUe 4 .19 3d Turtle Simulator game. Contribute to Oiboo/TRTL-Simulator development by creating an account on GitHub.github.com](https://github.com/Oiboo/TRTL-Simulator)

# Promote Your Bounty

**500,000 TRTL —** Currently I am seeking a pair of PHP hands that have the skill to implement some necessary connections to a particular API database, and implement it into a Wordpress website. Not completely being able to foresee all the tasks but I believe it will be a one-time effort, realisable in a day, spread over two weeks. Please PM me for more information. **— 476190.47619047**

# Community Advertising

![]({{ site.baseurl }}/images/0sBR7cPf2JWlRj5q3.png)

Hey! I just wanted to remind you guys the best server to sync your wallet with is still [turtlenode.online](http://turtlenode.online/)! Thanks! **\-Morpheus**

# Shoutouts & Thanks

**Sups** — Great support from Belorion in helping get the Nibblebox all in one miner running smoothly for NibbleClassic!

**funkypenguin** — Shoutout to @Rock’s new avatar, which is scary-as-hell (gah, i changed it before i saw this — rock)

**anon** — fuck you rock i know u read this

**dsanon** — ❤ the turtlecoin community.

**anonymous** — will you go to prom with me zpalm

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-feb-4-2019/)_._
