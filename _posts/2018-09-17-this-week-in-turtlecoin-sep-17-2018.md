---
layout: "post"
title: "This Week In TurtleCoin (Sep 17, 2018)"
description: "This week on Krang — I hit some walls with Rancher and decided to focus on a more traditional basic solution. This is a nice to have feature but can be included later. — Started on a simple python…"
image: "{{ site.baseurl }}/images/09egc0kf9rb8dnfPD.jpg"
date: "2018-09-17T14:40:49.174Z"
---

# Developer Updates

![Krang](https://miro.medium.com/max/1400/0*9egc0kf9rb8dnfPD.jpg)

Krang

**This week on Krang** — I hit some walls with Rancher and decided to focus on a more traditional basic solution. This is a nice to have feature but can be included later. — Started on a simple python Script that will (Work in progress)

1. _Setup the Terraform pre-requisites for each provider on the client system (Complete)_
2. _Initially Krang will support Digital Ocean and Linode (fexra’s request)_
3. _Once checks and setup is complete Krang.py will be able to deploy a testnet onto the provisioned computer using a combination of ansible (config management) and docker (application) (Working on this week — 50% complete)_
4. _Once done the TestNet can be destroyed (to be completed)_  
   **NOTE:** Initial release will focus on functionality, Flexibility (more providers with custom deployments) will be the focus after a working product is available.  
   I will be working closely will Fexra this week as he is working on a Web Frontend to deploy, manage and monitor the TRTL stack. Seems like a great opportunity to TRTL power it up and add a frontend to Krang. I’m sure Fexra will include it in his Weekly update, right Uncle Rock! :-) -Slash-atello

[4Reallive/krangThe TurtleCoin Blockchain Automation Suite. Contribute to 4Reallive/krang development by creating an account on GitHub.github.com](https://github.com/4Reallive/krang)

![]({{ site.baseurl }}/images/0ZrXPKeQtSlsIzQVI)

**Pool Interview w/ Cision —** The latest installment of the small pools series highlights Cision’s pool turtle.atpool.party which was one of our earliest pools. This series highlights smaller pools to help decentralize the hashrate to balance out mining power. **— RockSteady**

<https://blog.turtlecoin.lol/archives/interview-w-cision-from-turtle-pool-party/>

[Interview w/ Cision from Turtle Pool PartyRockSteady - Thanks for taking the time to do this interview. The purpose of the interview series is to help spread out…blog.turtlecoin.lol](https://blog.turtlecoin.lol/archives/interview-w-cision-from-turtle-pool-party/)

**TurtleCoin v0.8.3 Released** — This version is hopefully one of our most stable. Many improvements went into this release, and a lot of hard work went into it as well. This release lays the groundwork for a system that allows us to disconnect old clients from the network during fork upgrades to reduce the chances that legacy clients poison consensus. The fork at 800k was a little bit rocky at first, because we didn’t account for the mixin 7 transactions that would be in the mempool during the switch to mixin 3, which caused miners to be unable to create block 800,000\. The solution was to custom-build a daemon that would only pump out empty blocks, and running that on a pool until we were sufficiently far away from block 800,000 where the legitimate block-producing, transaction-processing v0.8.3 could be used. Thanks for everyone’s time who stayed awake to watch the change and help us along. **— RockSteady**

[http://latest.turtlecoin.lol](http://latest.turtlecoin.lol/)

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoinlatest.turtlecoin.lol](http://latest.turtlecoin.lol/)

<https://github.com/turtlecoin/turtle-network-cli>

![WalletShell Screens](https://miro.medium.com/freeze/max/60/0*v7tswYRN16KNa9p0.gif?q=20)

![WalletShell Screens](https://miro.medium.com/max/1200/0*v7tswYRN16KNa9p0.gif)

[turtlecoin/turtle-network-cliTRTL network status command line interface. Contribute to turtlecoin/turtle-network-cli development by creating an…github.com](https://github.com/turtlecoin/turtle-network-cli)

![TRTL-CLI-PY](https://miro.medium.com/max/60/0*s9Z4TjlUZBS2T1Ch.png?q=20)

![TRTL-CLI-PY](https://miro.medium.com/max/850/0*s9Z4TjlUZBS2T1Ch.png)

TRTL-CLI-PY

**TRTL-CLI-PY** — I rewrote mrrovot’s TRTL CLI in python, so that I could add my own changes to it. It does everything TRTL CLI does, and more! Thanks to zpalm for helping me optimize it a bit, and big shoutout to Xaz and mrrovot who wrote this tool in the first place! Check it out ;) **— Sajo8**

<https://github.com/sajo8/trtl-cli-py>

![Turtacus](https://miro.medium.com/max/60/0*dpmyljN7G3zdQgjU.jpg?q=20)

![Turtacus](https://miro.medium.com/max/1400/0*dpmyljN7G3zdQgjU.jpg)

Turtacus

[Sajo8/TRTL-CLI-pyrewrite of @mrrovot's TRTL-CLI-py. Contribute to Sajo8/TRTL-CLI-py development by creating an account on GitHub.github.com](https://github.com/sajo8/trtl-cli-py)

<https://www.github.com/rynemgar/gladiator-bot>

![T-Scripta](https://miro.medium.com/max/60/0*9_5_FRIi1KZo5dAv.png?q=20)

![T-Scripta](https://miro.medium.com/max/1226/0*9_5_FRIi1KZo5dAv.png)

T-Scripta

[Rynemgar/Gladiator-BotContribute to Rynemgar/Gladiator-Bot development by creating an account on GitHub.www.github.com](https://www.github.com/rynemgar/gladiator-bot)

<https://github.com/turtlecoin/turtle-wallet-tscripta>

![]({{ site.baseurl }}/images/0bs2EPb5VPSCyxRJJ.png)

[turtlecoin/turtle-wallet-tscriptaTurtlecoin Wallet made in C# WPF. Contribute to turtlecoin/turtle-wallet-tscripta development by creating an account on…github.com](https://github.com/turtlecoin/turtle-wallet-tscripta)

[https://shellnet.pw](https://shellnet.pw/)

![]({{ site.baseurl }}/images/0Fq0rgr7Ss3yXo-\_2.png)

[Shellnetcreate an accountshellnet.pw](https://shellnet.pw/)

Also, there was another patch to make the node connection shut down a lot faster in the wallet — not a big thing but it should make shutting down a lot more responsive.

I meant to put this in a roundup a few weeks back, but zedwallet on Windows now has auto-complete support, to bring it up to par with Linux and Mac.  
This works anywhere you have options of commands to pick, like the open menu, the main menu, and the ‘node not open’ menu. Saves you a tiny bit of time if you’re lazy ;)

Hopefully you’ve been liking the new menu system if you’re using 0.8.3 — note that you can type both the command names and the numbers, whatever takes the least effort :D

Meanwhile, I’m working on something bigger which will take some time… stay tuned!

- **zpalm**

![]({{ site.baseurl }}/images/0p80LjNK3jLgVnR-6.png)

**Web Wallet** — Busy applying changes to masari’s webwallet so it will work for Turtle. This includes, a project restructure to dotnet core (done), re-write of the background caching process to handle large chains (done), re-work of the client side crypto functions to work for TurtleCoin (done), re-brand for turtle and a few other minor things. Am currently working on some improvements to how mempool Tx’s are handled in the web wallet and am adding some additional info to be displayed if there are unconfirmed fusion transactions. **\-WhassupZA (Discord), Dave (GitHub)**

<https://github.com/turtlecoin/turtlecoin-webwallet-js/tree/development>

![]({{ site.baseurl }}/images/0aOIKkrLIiIWyQjmD)

**Nest** — Version 0.34 of Nest, your GUI wallet, was released this week. It has been intensively tested, so you will not encounter the issues we had in 0.32\. Please upgrade as it uses latest core 0.8.3, which is not compatible with previous versions. I think you will like the new address directory and wallet scan height features. If you are the maintainer of a fork of TurtleCoin, I made a guide to fork Nest for your coin. **— Jon Nest**

<https://github.com/turtlecoin/turtle-wallet-go/blob/master/docs/forking-nest.md>

<https://github.com/turtlecoin/turtle-wallet-go>

# Community Advertisements

![turtlecoinbuttons](https://miro.medium.com/max/60/0*46IFdFmi-40HXTB7.png?q=20)

![turtlecoinbuttons](https://miro.medium.com/max/1400/0*46IFdFmi-40HXTB7.png)

turtlecoinbuttons

Do you want some TURTLE merch like buttons and other assorted things? Then check out <https://zazzle.com/turtlecoinbuttons> for your TRTL needs. Also shout out to some other TRTL merch shops, like @bbanditt#3011 and @DonMatus#3519 on Discord! Give them a big round of applause!

<https://zazzle.com/turtlecoinbuttons>

![turtlenode.online](https://miro.medium.com/freeze/max/60/0*d6WggCvXESy8cpUB.gif?q=20)

![turtlenode.online](https://miro.medium.com/max/1400/0*d6WggCvXESy8cpUB.gif)

turtlenode.online

[TurtlecoinButtonsCheck out all of the amazing designs that TurtlecoinButtons has created for your Zazzle products. Make one-of-a-kind…zazzle.com](https://zazzle.com/turtlecoinbuttons)

[http://turtlenode.online](http://turtlenode.online/)

![FunkyPenguin](https://miro.medium.com/max/60/0*zs0jbI27WvMIteuo.png?q=20)

![FunkyPenguin](https://miro.medium.com/max/1400/0*zs0jbI27WvMIteuo.png)

FunkyPenguin

Curious re whether my contented VPS resources were negatively impacting my pool’s luck, I migrated the pool to Google Kubernetes Engine (recipe forthcoming). 800Kpocalypse aside, the pool does \_feel\_ luckier on GKE, and I now hope to sleep (more) soundly at night, and work on more Geeky Cookbook recipes ([https://geek-cookbook.funkypenguin.co.nz](https://geek-cookbook.funkypenguin.co.nz/))  
So, If you’re a geek who happens to like mining TRTL (among other geeky things), come and visit [https://trtl.heigh-ho.funkypenguin.co.nz](https://trtl.heigh-ho.funkypenguin.co.nz/), or jump into the “kitchen” discord (it’s not all mining) at [http://chat.funkypenguin.co.nz](http://chat.funkypenguin.co.nz/) Re the pool features, it’s all the usual features, my fav feature is a discord community, followed by telegram/email notifications on blocks discovered etc. This makes mining a more shared, enjoyable activity ;)

<https://geek-cookbook.funkypenguin.co.nz/>

[https://trtl.heigh-ho.funkypenguin.co.nz](https://trtl.heigh-ho.funkypenguin.co.nz/)

[Funky Penguin's Geek CookbookThegeek-cookbook.funkypenguin.co.nz](https://geek-cookbook.funkypenguin.co.nz/)

# Community Shoutouts

[Redirecting to Discord...Edit descriptionchat.funkypenguin.co.nz](http://chat.funkypenguin.co.nz/)

**Cision** — I want to thank GNU/iburnmycd™ that he havent blocked me yet and helping me to setup my public daemons :)

**CaptainJac0** — Thank you to everyone who voted for me on <https://www.rapdasa.org/design-competition/?contest=photo-detail&photo_id=6276>

**Judderz** — You want Turtle decals, come see me :)

**Oseru / Hasagi** — Amazing work by turtlenode.online for hosting a low tx fee node! Glad to use your node my man!

**Oseru / Hasagi** — Also a shoutout to Turtle?#3684 for his birthday! Expect a few shells sent your way on Monday. ;)

**Moneymind420** — Give big shout out to RockSteady !!! We love Turtles !!!

**anon** — zpalm’s voice gives me the tingles

**Khem Boi** — Shout out to all the forking projects including monkey tips, and shout out to all the new miners out there helping the network!

**Freeman** — riche en information, merci

**Captain Jac0** — Arrrrrr to all Turtles

![CaptainJac0's Pirate Flag](https://miro.medium.com/max/60/0*8Lh_PNcTuTZHcuqd?q=20)

![CaptainJac0's Pirate Flag](https://miro.medium.com/max/1078/0*8Lh_PNcTuTZHcuqd)

CaptainJac0’s Pirate Flag

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-sep-17-2018/)_._
