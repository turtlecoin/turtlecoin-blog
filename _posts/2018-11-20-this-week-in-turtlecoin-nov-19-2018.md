---
layout: "post"
title: "This Week In TurtleCoin (Nov 19, 2018)"
description: "Hunter Faucet — A new faucet has finally launched! Hunter Faucet is a TurtleCoin faucet with an extra twist to it! Referral links and special “Hunter Codes” are features of this faucet. Hunter Codes…"
image: "{{ site.baseurl }}/images/022r5szChIo87UFKq.png"
date: "2018-11-20T05:16:39.543Z"
---

![]({{ site.baseurl }}/images/022r5szChIo87UFKq.png)

# Developer Updates

![]({{ site.baseurl }}/images/0XE6PxyPKlAszgvkX.png)

**Hunter Faucet** — A new faucet has finally launched! Hunter Faucet is a TurtleCoin faucet with an extra twist to it! Referral links and special “Hunter Codes” are features of this faucet. Hunter Codes allow users to redeem more than the default amount of TRTL. Users can also create referral links so that they can refer other users to the hunter faucet for a small TRTL kickback. Happy hunting! **— Xaz**

[Hunter FaucetThis is a faucet for acquiring TurtleCoin, but with a twist! If you have an optional Hunter Code, enter it below for an…faucethunter.online](https://faucethunter.online/index.php)

![]({{ site.baseurl }}/images/0227x0ZJ9BiwPnrPg.png)

**Vendible —** Vendible’s vision is to be the solution for the future global economy by building an all-encompassing commerce ecosystem. We are completing an integrated eCommerce payment gateway which offers merchants access to traditional credit and debit payments alongside Bitcoin, PIVX, IoP, Litecoin, Ethereum, Ripple, Bitcoin Cash, Cardano, Monero, and Turtlecoin. Further developments will include a multi-currency wallet with brick-and-mortar POS functionality, a teller system for merchants which will facilitate exchange of digital assets, savings accounts, payroll and budgeting functionality, P2P payments, and more. We want to see adoption in communities which have cross-border ties as we see a tremendous opportunity for both merchants and users of the platform to transfer value. Vendible-to-Vendible transactions will not incur fees. We are led by founders and organization leaders from PIVX, IoP, Libertaria, and Sentinel and are creating a decentralized governance model where the people using the platform will decide the future of its development through a tokenized system which rewards use. **— Memnon**

[Discord - Free voice and text chat for gamersStep up your game with a modern voice & text chat app. Crystal clear voice, multiple server and channel support, mobile…discord.gg](https://discord.gg/57dQ2N9)

[Vendible | Integrated payments platformVendible offers you access to credit and debit payments alongside Bitcoin, PIVX, IoP, Litecoin, Ethereum, Ripple…www.vendible.org](https://www.vendible.org/)

![]({{ site.baseurl }}/images/0AGAMijoh7awoy4qQ.png)

**New! TurtleCities Upgrades!** — You can now double your storage from one floppy to a dual density floppy for a whopping total of 2.88mb of space on your TurtleCities account! The best compliment for so much room for activities is a Shell Account! That’s right, with the help of a Telnet session, you can connect to a remotely hosted linux shell account, just for you! Get one today! Now, currently offering BASH, FISH and ZSH! Note to those waiting on the list, I only check about once a week or two, so if you’re waiting for your account to be activated, ping me in the discord chat and I’ll usually be able to set you right up. **— Rock (Chief Donut Officer, TurtleCities Intl.)**

[TurtleCities™Edit descriptionpages.turtlecoin.lol](http://pages.turtlecoin.lol/)

![]({{ site.baseurl }}/images/02VPZ1qeOgB85IidN)

**TurtlePay™ Explorer** — TurtlePay™ has been making moves with a completely rewritten explorer with a brand new caching mechanism that makes it super fast. To tell you the truth, I promised IBMCD I’d write something about it, but it’s about midnight and the bedtime beers are taking me, and I last second remembered the fact that I forgot to write this about two seconds before hitting submit. phew! — Rock

[TurtlePay™: Fun, Fast, & Easy Crypto PaymentsEdit descriptionturtlepay.io](https://turtlepay.io/)

![]({{ site.baseurl }}/images/0hyfYMxnnNEPilC9Y.png)

![]({{ site.baseurl }}/images/0tFi_lG3U3CJO4oQT.png)

![]({{ site.baseurl }}/images/06WiNc7eWVCCfKuLu.png)

As some of you turtles may know, TurtleWallet is powered by TRTL.Services, which provides the backend logic and automation for creating addresses and processing payments and comes with an frontend API. The last month and a half I been extensively testing the platform with the help of TurtleWallet, which is currently the only active app build on top of this.

In the coming days, I will publish a detailed article dedicated to TRTL.Services — with all its upcoming features and nifty tools, but for this article I will primarly focus on TurtleWallet. I’m very excited to report that since the launch date of TurtleWallet (39 days ago), we have had no major incidents or bugs to report. However, as you all know this does not mean that there was a lot of room for improvement! Hence, this week I will be upgrading TurtleWallet and TRTL.Service and wanted to share some screenshots.

Statistics (39 days)  
— 309 users  
— 386 accounts  
— 7,181 transactions  
— 69,596,355.10 TRTL processed in payments  
— 311,383.99 TRTL in collected service fees  
— 1,357,557.81 TRTL in operation costs

New Features + Fixes:  
— Export sub-address keys support  
— Activity details (modal overview)  
— Graph bug fix + design improvement  
— Accurate conversion to 12 decimals for in total of 50 cryptocurrencies, fiat currencies and assets.  
— Recaptcha on login / register  
— Rate limiter on transfers  
— Account Oversight UI improvement  
— Dependency + library upgrades (including client side)  
— Improved transaction confirmation tracking  
**Fexra**

[TurtleCoin Web Wallet | TurtleWalletEdit descriptionturtlewallet.lol](https://turtlewallet.lol/)

![]({{ site.baseurl }}/images/0JtakY65zFJ-te0H8.png)

**rainborg —** I just wanted to give a brief update on RainBorg, as I know a few of you noticed she’s gone through some changes recently. Originally I was hosting her on a GCP server that I could no longer afford to run, so a member of our community stepped in to run her. Once they could no longer run her either, she went down for 2 weeks or so while looking for a new host. Thankfully Z stepped in and he now runs her! Beyond hosting, she’s also been getting some updates over time. A few weeks back she was updated to RainBorgCore (AKA RainBorg 2.0), which gives cross-platform support, and since then I’ve been slowly adding and changing things here and there to make her be more adaptable to our community’s forked coins that are starting to use the tip bot for their own coins. Once she’s fully ready for primetime, I’ll be ahead and do a small write-up on how to deploy her as well as tip bot for other coins. Also, while I’m here writing, here are her current top stats:  
Total TRTL Sent: 7,203,876.8 TRTL  
Total Tips Sent: 53,097  
Average Tip: 135.67 TRTL  
**Canti**

[BrandonT42/RainBorgCoreAn updated, more efficient, and cross platform implementation of RainBorg. Easier to port to other currencies, more…www.github.com](https://www.github.com/BrandonT42/RainBorgCore)

![]({{ site.baseurl }}/images/0C62OZIJDB2VXzxjB.jpg)

**Traveling around Australia —** We are currently traveling around Australia showing people on the road and around where ever we go Turtle Coin. Since embarking on this expedition we had had truck drivers call us on the radio and ask what is a Turtle Coin and it has also been a conversation starter in some caravan parks where people are curious what a Turtle Coin is, some people have been interested and some not so interested once they find out it’s crypto related. If you are in Australia and have seen the van gives us a shout on discord and let us know. Later on in our travels we plan to stop at a Turtle breeding beach and see if we can either leave a sticker with them and maybe donate some turtles to some turtles. **— aneki**

![Image result for bricks of cocaine](https://miro.medium.com/max/60/0*e_soNK4R4wir1q04?q=20)

![Image result for bricks of cocaine](https://miro.medium.com/max/1240/0*e_soNK4R4wir1q04)

**lite-blocks —** Last week I have detailed you guys what are lite-blocks and how do they work.. and here is the update in its development.. I have finished the necessary functions required to handle lite-blocks and request any missing transactions.. The only left-over thing is to add CLI-option to activate lite-blocks and logic to determine which peers support lite-blocks and which do not.. I hope with the help of iburnmycd, I can complete those things within no time..(bcoz he was responsible for the code which kicked unsupported nodes and also for the new CLI-options which will be in the next release) **— rashedmyt**

[rashedmyt/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - rashedmyt/turtlecoingithub.com](https://github.com/rashedmyt/turtlecoin/tree/lite-blocks)

![]({{ site.baseurl }}/images/0fVhjMWfrtmR_I4Hy.png)

**Shellnet is ready for forking! —** The amazing Shellnet webwallet is now more forkable than ever. As it turns out, forking TurtleCoin gives you access to a ridiculous suite of complementary software and services. In fact, you can now get a very solid web wallet with very little effort! Check out my WIP forking guide for Shellnet! **— jerme404**

[jerme404/shellnet-webwallet-goA turtlecoin web wallet WIP. Contribute to jerme404/shellnet-webwallet-go development by creating an account on GitHub.github.com](https://github.com/jerme404/shellnet-webwallet-go/blob/master/docs/forking-guide.md)

**TRTL-CLI-py —** I added support for cryptonote.social for the pool stats so it won’t crash anymore. Yay! I’ve also made progress on a command where you can grab detailed stats of all the pools at once, should come out in a few days **— Sajo8**

[turtlecoin/TRTL-CLI-pyrewrite of @mrrovot's turtle-network-cli... in python :purtle: - turtlecoin/TRTL-CLI-pygithub.com](https://github.com/turtlecoin/trtl-cli-py)

![]({{ site.baseurl }}/images/1Q0hleMcg-ElGMrqNFfQD-g.png)

**Medium Article** — I thought I would write my thoughts on the importance of TurtleCoin. **— Alien**

[A TurtleCoin TestimonyEdit descriptionmedium.com](http://blog.turtlecoin.lol/@AlienTurtle/a-turtlecoin-testimony-b9ccb482cf38)

![]({{ site.baseurl }}/images/02AVS6dmU96cYmSG0.jpg)

**Rewriting all the things! —** Now that I finished rewriting the wallet backend, I decided to start rewriting turtle-service, to use the new backend. I found a nice HTTP server library, and stuff was going well, but I was hitting a segfault when closing a wallet and reopening a new one.  
Basically what was going on is the NodeRpcProxy takes a reference to some logger objects, and when we destroy the wallet instance, they go out of scope. Normally, the NodeRpcProxy would be destroyed as well, however, since the code is a bit dodgy, the shutdown() routine doesn’t really work.  
To get round this, instead of waiting for it to shutdown, I simply detached the thread, leaving it running in the background to shutdown in it’s own time. However, since it takes references to these loggers, which are now out of scope, it crashes when trying to write a message to them. I attempted a fix, but then I got an even weirder error which I couldn’t figure out how to fix.  
I said screw it, I’ll just rewrite the NodeRpcProxy then. I haven’t though of a name for it yet, so I’m calling it Nigel. It shouldn’t be too tricky to use, since I can use the same nice HTTP library I’m using, and a nice JSON library. Hopefully, then Valgrind (a memory checker) will help me find bugs — When you run it currently, the code has so many bugs it prints out a few hundred a second so you can’t find out what’s wrong :(  
Back to the API — This will hopefully be a lot nicer for developers to use than current turtle-service. For one, you’ll open/import wallets via the API. This has a massive bonus of you not having to parse log files to find out if the wallet opened successfully or not.  
Second, you’ll be able to swap nodes without having to close turtle-service. This will allow for richer experiences where the software can detect if your node appears to have gone offline, and can offer or automatically swap to another node.  
It’s also using a more REST-like API — Thanks to Iburnmycd for helping me with this. I’m using Swagger (http://editor.swagger.io/) for the documentation — nice find Fexra — Which along with generating a really nice UI, will also generate API wrappers in something like 40 different programming languages for you — super cool! **— Zpalm**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/tree/wallet-api)

# Community Advertising

- Get any SkillShare course in exchange of turtle coin. Any course (Including Premium Course) will be given in exchange of 7350 Turtle Coin. I am on discord server steve#7423
- Looking for the basic links for Turtle? Look no further! (Plus some nodes!) Give Japakar’s site a looksie. Theres no naked ladies but there are links! — [http://turtle.japakar.com](http://turtle.japakar.com/)

# TRTL Bounties

100k — Get TRTL listed on DELTA Direct. — MrSquiggle  
This had been completed already at the time of it being posted. (I’ll still claim it if the 100k is up for grabs however :D — rock)

# Shoutouts & Thanks

**Sajo8** — Shoutout to mose_forge for providing these dope turtlecoin swag!! <https://cdn.discordapp.com/attachments/471023390954618883/513146088891482114/image0.jpg>

**rogerrobers** — Shout out to rynem for giving me a site — totalcarnage.turtacus.com is dedicated to the one and only Captain Ginyu

**greywolf —** thanks to Catgirl and DiscoTim for hosting another great bingo party! there were over 50 turtles enjoying games of bingo and some slots payouts; with lots and lots of friendly chatter.

**anon** — who farted?

**japakar —** Everyone at Turtlecoin in Discord :) You guys are awesome!

**rock** — shout to rashed, canti, fexra, ibmcd, and zpalm for their hard work this week on the core suites!

**rock** — shoutouts to rogerrobers for being the first person to upgrade to a dual density floppy on his TurtleCities page!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-nov-19-2018/)_._
