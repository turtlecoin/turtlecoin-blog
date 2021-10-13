---
layout: "post"
title: "This Week In TurtleCoin (Jan 1, 2019)"
description: "Happy new year! It’s been a great year with you all, and I hope you’ve all made the resolution to mine more TRTL this year, because we’ve got a heck of an update for you! Read more about the upcoming…"
image: "{{ site.baseurl }}/images/0pfieqQEst0UxtGCh.png"
date: "2019-01-03T04:56:25.606Z"
---

![]({{ site.baseurl }}/images/0pfieqQEst0UxtGCh.png)

Happy new year! It’s been a great year with you all, and I hope you’ve all made the resolution to mine more TRTL this year, because we’ve got a heck of an update for you! Read more about the upcoming PoW upgrade! 30 days!

[Proof-of-Work Algorithm ChangeThe core development team has observed the fact that the network hash rate has climbed substantially over the last few…blog.turtlecoin.lol](https://blog.turtlecoin.lol/archives/proof-of-work-algorithm-change/)

# Developer Updates

![]({{ site.baseurl }}/images/0X8Z0TM3IRch3qXcF.png)

**TurtlePay™ —** I’m proud to say that the TurtlePay™ Public Beta launch occurred as promised just before Jan 1 2019 00:00:00 GMT. For those of you that have not been following the development of the project, there’s quite a bit of work going on behind the scene to make TurtlePay™ an awesome tool for developers. The service is FREE for everyone to use and the only fee is the standard network transaction fee of 0.10 TRTL.  
TurtlePay™ is a payment processing service that is designed to help developers integrate TurtleCoin™ payments into their existing applications. By providing an easy to use set of tools to incorporate TurtleCoin™ payments into more applications, we hope to drive adoption of the technology to new heights.  
Some people just want to write cool applications and develop new tools that allow them to use the technology without worrying about how it works, why it works, or keeping up with the latest and greatest features. Let us worry about the hard parts while you build awesome applications that use TurtleCoin™.  
We’re looking forward to see what kind of cool things people start to build based on the platform. We’ve already identified a few tweaks to the current system that need to be made given some of the feedback a few people have provided.  
In the next few weeks, I’ll be building out additional documentation on how to leverage the full power of TurtlePay™ and its related tools as well as adding additional features that will only make the platform better.  
The platform is designed with scalability in mind and can easily grow as the needs of community grows. You can even run the platform yourself! Stay tuned for further updates**! — IBurnMyCD**

[TurtlePayTurtleCoin payments processing for developers, by developers.turtlepay.io](https://turtlepay.io/)

![]({{ site.baseurl }}/images/0x_Ppt3LYAmErzApL.png)

**Mobile Wallet —** A lot of people have been asking about a mobile wallet, so I thought I’d give it a shot. I’ve got a simple UI running on the phone, simply generating wallets and not much more yet.  
I’m working on building out the main wallet functionality in a separate node package (https://github.com/zpalmtree/turtlecoin-wallet-backend) so it can be used for other things — think web wallets, native GUI wallets that don’t need any of the C++ code, etc. For that reason the repo will be pretty quiet until I’ve got that sorted out. Once the backend is done, it should just be a small matter of hooking it up and making everything look pretty, then off to the races.  
This is going to be a native mobile wallet, so it’s not just a web wallet wrapped in an app. Furthermore, you’ll own your own private keys. This does mean you’ll have to scan the chain, which might be a bit heavy on CPU and battery life, but if you create a new wallet rather than importing, it shouldn’t be too bad. **— Zpalm**

[zpalmtree/ton-chanA mobile TurtleCoin wallet. Contribute to zpalmtree/ton-chan development by creating an account on GitHub.github.com](https://github.com/zpalmtree/ton-chan)

![]({{ site.baseurl }}/images/0bJ0dZB-syBmFC4aP.png)

**TurtleCoin RPC Nim** — This is a Nim wrapper for the TurtleCoin RPC APIs. It includes two modules, \`walletd\` for wallet JSON RPC commands and \`turtlecoind\` for the daemon HTTP and JSON RPC methods. There is also a simple example on github showing how to use this package. I have been learning Nim for about a month so let me know if there are any bugs! **— DSanon**

[anonanonymous/turtlecoin-rpc-nimA nim wrapper for the turtlecoin rpc interface. https://api-docs.turtlecoin.lol - anonanonymous/turtlecoin-rpc-nimgithub.com](https://github.com/anonanonymous/turtlecoin-rpc-nim)

![]({{ site.baseurl }}/images/00Yqn0S4UuwmgTiie.gif)

**TurtleCoin-Utils —** I’m happy to report that the TurtleCoin node.js utilities are almost complete. This package is designed to provide native JS (and TypeScript — Thanks Z!) methods and calls that work in Node and in browser to create addresses, decode addresses, scan transactions for funds, create new transactions, and even generate the ring signatures necessary to create a valid transaction on the network. I’ll be working on improving (and in some cases creating) the documentation for the package in the coming days to make the entire package easier to use. **— IBurnMyCD**

[turtlecoin/turtlecoin-utilsNode.js utilities for working with the TurtleCoin network - turtlecoin/turtlecoin-utilsgithub.com](https://github.com/turtlecoin/turtlecoin-utils)

![]({{ site.baseurl }}/images/0M9yggulkqj-OK7Pi.gif)

**Turtacus —** Turtacus has been rapidly draining funds recently with very few donations coming in to support him. For that reason, I have begun looking at new ways for his prizes to be generated and funded. In coming time, I will be changing the way the tournament works. There will be an entry fee which will only allow those people who have entered, to make it onto the leaderboard. Anyone will be able to fight but only those entered will gain points for the tournament. On top of this, there will be a new points system for the tournament whereby winning will net you 2 points, losing will net you 1 point. In this way, participation is encouraged win or lose. The entry fee is yet to be decided but will likely be between 2500 and 5000 TRTL per person since this is an easy sum to acquire even just from tips during the week. The tournament prize will be 90% of the overall entry fees collected, with the other 10 % going to Turtacus’s prize fund which will be added to an occasional tournament prize pot. As you can tell, there are a lot of changes coming. It will take time but hopefully, it will encourage more fighters. **— Rynem**

[Rynemgar/Gladiator-BotContribute to Rynemgar/Gladiator-Bot development by creating an account on GitHub.www.github.com](https://www.github.com/rynemgar/gladiator-bot)

![]({{ site.baseurl }}/images/00WQA37BFs3PVY-tb.gif)

**New Turtle-Service API** — To any developers who are currently developing apps with turtle — I would love if you would try out my new API — It’s a replacement for turtle-service, and it gives a bit of a friendlier, REST based interface. If you are having trouble getting it working or have any queries, let me know and I’ll be happy to help. **— zpalm**

[TurtleCoin Wallet API DocumentationEdit descriptionwww.futuregadget.xyz](https://www.futuregadget.xyz/api-docs/)

# Promote Your Bounty

**250,000 TRTL** — Integrate popular hardware wallet from SatoshiLabs, Trezor T in TurtleCoin’s Nest wallet in order to create and encrypt, decrypt wallet and sign transactions with the device. **— Elkim**

![teacup made this :D](https://miro.medium.com/max/60/0*i7m-jY_JvJ5pI904?q=20)

![teacup made this :D](https://miro.medium.com/max/1400/0*i7m-jY_JvJ5pI904)

Teacup made this :D

# Community Advertising

Tired of all that hard work in the turtle mines, and just want a little bit of TurtleCoin for free? C’mon over to the Llama & Horse TurtleCoin Faucet! <https://trtl.faucet.llama.horse/> It runs a little differently from the other faucets, but we hope this leads to it being self-sustaining in the long-run.

[TurtleCoin FaucetAltcoin faucets provided by Llama and Horse Mining Co.trtl.faucet.llama.horse](https://trtl.faucet.llama.horse/)

Come join us and help our ducks find turtles. We are a small TurtleCoin mining pool looking to grow. Low fee and friendly discord channel (link on site)

[Muxdux Turtlecoin Mining PoolEdit descriptiontrtl.muxdux.com](https://trtl.muxdux.com/)

# Shoutouts & Thanks

Massive shoutout to MadHatter for building the Nibblebot! You can now send & receive NBX as tips in the NibbleClassic server! — Sups

HAPPY NEW YEAR TURTLES!!! — Turtley McTurtleton

Thanks everyone for a wondrous year! You are all amazing! Here’s to next year! — Oiboo

Shout out to the whole community on such a great year and for helping each other out no matter the problem! Can’t wait to see what 2019 brings. — Khem Boi

2019 will be big for TurtleCoin — mkid

Happy 2019 @ everybody — if(true)

Thanks for the last year, its been a blast! Looking forward to next year! Great community and group! — japakar

Thanks to all turtles fot a year full of inspiration and fun(bearbeitet) — bernd

happy new year turtlecoin and lads ❤ — mufalo

Thanks Rynem for creating Colosseum! Thanks community for the donations to it and the work he put into it! — Rynem

shoutout to the whole TurtleCoin community for a great first year, and ending of 2018\. you’re a fun group of people, and our developers keep working hard. thanks for making it real, gang. — greywolf

Z, you’re just plain awesome. I appreciate the banter you provide and look forward to a mobile wallet soon™. — ibmcd

Dear Dominos, we’re through. — Rock

Thanks to @ibmcd and all the turtlecoin community to have patience and keep teaching me new programming stuff every time I come — mrrovot

Shoutout to CapEtn for helping to test lots of my code. It’s great to have people using my code before it goes live so we can fix all the bugs! — zpalm

To any developers who are currently developing apps with turtle — I would love if you would try out my new API (https://www.futuregadget.xyz/api-docs/) — It’s a replacement for turtle-service, and it gives a bit of a friendlier, REST based interface. If you are having trouble getting it working or have any queries, let me know and I’ll be happy to help. — zpalm

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-jan-1-2019/)_._
