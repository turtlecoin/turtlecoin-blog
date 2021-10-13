---
layout: "post"
title: "This Week In TurtleCoin (FEB 10, 2019)"
description: "In this better late than never edition of the weekend roundup, we test our skills of survival while waiting for the Comcast guy! TurtleCoin + Alpine + Docker — I’ve managed to get the TurtleCoin…"
image: "{{ site.baseurl }}/images/0EvsoiWT07qdrrMYy.png"
date: "2019-02-15T14:34:34.179Z"
---

![]({{ site.baseurl }}/images/0EvsoiWT07qdrrMYy.png)

In this better late than never edition of the weekend roundup, we test our skills of survival while waiting for the Comcast guy!

# Developer Updates

![]({{ site.baseurl }}/images/0nwM11Bd5hAgJniiZ.png)

TurtleCoin + Alpine + Docker — I’ve managed to get the TurtleCoin binaries to compile on Alpine. There were a couple of issues that were preventing this. The first issue is that ucontext was deprecated in POSIX which musl adheres to. Thankfully someone had created a library that solves the problem. The second issue was that musl has a PAGE_SIZE macro defined in limits.h that was conflicting with a parameter used on slow-hash.c. This has now been changed to page_size in the core, resolving the conflict. So far, I’ve created three images. The first image, which is meant to be a starting point for your own images, builds all the binaries in Alpine then copies them to a scratch container resulting in an image size of 22.6MB. The zedwallet container comes in at 7.96MB and the TurtleCoind image, which includes checkpoints, is only 90MB. I plan to create a series of docker-compose files that will tie them together to help accomplish various tasks. You can view the images on Docker Hub: <https://hub.docker.com/r/andrewnk/turtlecoin> or on github: <https://github.com/andrewnk/turtlecoin-docker> — andrew | trtl.rocks

[andrewnk/turtlecoin-dockerDockerfiles and docker-compose files to run various TurtleCoin software and projects - andrewnk/turtlecoin-dockergithub.com](https://github.com/andrewnk/turtlecoin-docker)

![Image result for unreal engine](https://miro.medium.com/max/60/0*86SscXmgh7OY7x6Z?q=20)

![Image result for unreal engine](https://miro.medium.com/max/1400/0*86SscXmgh7OY7x6Z)

Turtle Simulator UE4 — Turtle Simulator has now been uploaded to GitHub! If you want to help with the project, or if you if you are interested in game design, check out the code and give me a message in #Dev_gaming channel! Im looking for anyone who knows: 3d Modeling/ Animation/ UV maps. Coding in UE4, Blueprints or C++ Music /Audio Ideas / Level design It’s a massive project I’ve undertaken so any help takes something off my to-do list. Thanks in advanced! Looking forward to see what we can make together! Oiboo P.s No minimum skill level, all help will be appreciated! — Oiboo

[Oiboo/TRTL-SimulatorUe 4 .19 3d Turtle Simulator game. Contribute to Oiboo/TRTL-Simulator development by creating an account on GitHub.github.com](https://github.com/Oiboo/TRTL-Simulator)

![]({{ site.baseurl }}/images/0K-WDu843LHzbLDwf.png)

TRTL.rocks — I’ve made several improvements and changes to the website. I made a silly logic error that caused the initial load time to vary drastically or stall altogether. If the node or pool API is not accessible, then it won’t be shown on the site. If you don’t see your node or pool in the list, this is most likely the reason. I’ve cleaned up the line chart, including formatting y-axis and point labels, which should help readability. I’ve added tooltips to most table headers that describe what the column represents. These can be turned on or off by toggling the Tooltips switch on the bottom right hand of the screen. Finally, I’ve added the ability to switch the line chart between live and historical data. On initial load, the live mode will be enabled and updates are displayed whenever the data is pushed from the database. I’m in the process of rewriting iburn’s blockexplorer-cache library to use sequelize, which will help me move on to the block explorer portion of the site. — andrewnk | trtl.rocks

[andrewnk/turtle-explorerContribute to andrewnk/turtle-explorer development by creating an account on GitHub.github.com](https://github.com/andrewnk/turtle-explorer)

# Promote Your Bounty

500,000 TRTL — Currently I am seeking a pair of PHP hands that have the skill to implement some necessary connections to a particular API database, and implement it into a Wordpress website. Not completely being able to foresee all the tasks but I believe it will be a one-time effort, realisable in a day, spread over two weeks. Please PM me for more information. — 476190.47619047

1,218,917 TRTL — Will buy developer license for Turtle wallet app — mikeykones

# Fork Watch

![]({{ site.baseurl }}/images/0OV3mS6H0XkMif7-f.png)

## Excelsior

The Celestial community called out.. And the call was answered. We couldn’t save the existing chain, so we re-forked, gave it a new name, and launched Excelsior on Sunday the 3rd of February. All the same network settings the previous dev. gave it, just a new name, logo, and updated codebase.  
If you don’t know Celestial; it was the first coin using the CN Soft Shell algorithm, by TurtleCoin (now with Lite Blocks by Rashed!).  
**Supply**; 1,700,000,000.00000  
**Premine**; 11,000,000.00000 (for 1:1 swap for existing mined coins)  
**Block Reward**; (Approx) 100.64280 XLS  
**Emission** speed factor: 24  
**Find us** on the web; [http://xlscoin.info](http://xlscoin.info/) Join us in our Discord; <https://discord.gg/rhfW9jZ>

![lithe-logo.png](https://miro.medium.com/max/60/0*fE_JaT_1YA2kO0mq?q=20)

![lithe-logo.png](https://miro.medium.com/max/500/0*fE_JaT_1YA2kO0mq)

## Lithe™

It’s everything DASH intended to be but without Masternodes.  
<https://github.com/lithe-project>

# Community Advertising

![]({{ site.baseurl }}/images/0Itm6N8sNntfr0zPO.png)

2 nodes, twice the fun! turtle.japakar.com

![]({{ site.baseurl }}/images/0_ECijp3OFl6Zm4gt.png)

Hey! I just wanted to remind you guys the best server to sync your wallet with is still turtlenode.online! Thanks! -Morpheus

# Shoutouts & Thanks

Great support from Belorion in helping get the Nibblebox all in one miner running smoothly for NibbleClassic! — Sups

Shoutout Birmingham iron and the aaf!! Go Luis Perez 💪 — rogerrobers

Shout out to me, Dio! — khem Boi

Shouts out to IBMCD for his work with multisig! — rock

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-feb-10-2019/)_._
