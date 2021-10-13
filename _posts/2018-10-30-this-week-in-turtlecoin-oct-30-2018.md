---
layout: "post"
title: "This Week In TurtleCoin (OCT 30, 2018)"
description: "On this spooky edition of the TurtleCoin weekly roundup, we brag about our accomplishments and eat candy until our eyeballs turn green! If you’d like to be included in next week’s roundup, type !tag…"
image: "{{ site.baseurl }}/images/0AoarOmNgOZSrfVFT.png"
date: "2018-10-30T18:24:13.229Z"
---

![]({{ site.baseurl }}/images/0AoarOmNgOZSrfVFT.png)

_On this spooky edition of the TurtleCoin weekly roundup, we brag about our accomplishments and eat candy until our eyeballs turn green! If you’d like to be included in next week’s roundup, type_ `_!tag roundup_` _in the chat for the links to submit your updates!_

![]({{ site.baseurl }}/images/0wTEpN7QnLYEoBUOo.jpg)

# Developer Community

**WalletGreen / turtle-service rewrite —** Forgot to give updates in the last few round-ups, lol. Work continues on my wallet rewrite. The most notable features I’ve implemented recently are transactions.

Transactions are surprisingly tricky to get working in cryptonote coins, and the way they work is pretty darn confusing! I plan on writing an article on this at some point, because it took me quite some time to work out from the current code, and it would be nice to have a good explanation written down somewhere.

I still need to implement fusion transactions, but I think this will be pretty trivial, as they are essentially just a standard transaction with some constraints.

Also implemented were some poor man’s events. They’re not a first class citizen in C++, but we can make some pretty decently working events which allow us to fire off a chunk of code when something happens, such as a transaction being received, or the wallet syncing.

![zpalm's even handler](https://miro.medium.com/max/60/0*C8srHJ6a7OJ2D4e5.png?q=20)

![zpalm's even handler](https://miro.medium.com/max/1400/0*C8srHJ6a7OJ2D4e5.png)

zpalm’s even handler

Another cool thing is the wallet file format (partially shown in the first image). It’s all nicely structured JSON (once decrypted with the password). JSON works in pretty much every language so this will help programmers interact with wallets in other languages with more ease. Furthermore, the wallet encryption is done using AES encryption, with passwords hashed with PBKDF2\. This is both present in many programming languages, and the use of PBKDF2 allows to make brute forcing wallet passwords a slow operation.

I recently tested syncing my personal wallet with this rewrite, and I was glad to see the balances matched up exactly. Also worth noting is that the file was only 16MB compared to 57MB using a standard wallet program, a space saving of over 3.5x!

Finally, I implemented node fees. That one was pretty simple to do. I need to add some code to be able to correctly lock and unlock funds when they are moving from the mempool into a block, or from the mempool back into your wallet, if they get cancelled for some reason. Once that’s done, I can start work on adding all the API calls needed to build wallets. **— zpalm**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/tree/walletgreen-rewrite)

![]({{ site.baseurl }}/images/0RiVLAndircgm2L3C.png)

**turtlecoin-rpc-php —** What’s up turtles! v2.0 of the PHP RPC wrapper was pushed last week. Prior to this release, this wrapper could talk with walletd/turtle-service. In 2.0, support was added for all of the turtlecoind RPC methods, and the name of the composer package was changed from `turtlecoin/turtlecoin-walletd-rpc-php` to `turtlecoin/turtlecoin-rpc-php`. The PHP examples in the API docs (<https://api-docs.turtlecoin.lol/>) were updated to reflect these changes. This update also includes a few new methods to make it a little easier and cleaner to work with the response details (i.e. `$response->toJson()` or `$response->toArray()` or `$response->results()` to access the results field in the response as an array). Check the repo README for details (hook us up with some GitHub stars while you're there :D). More to come. **\- tmac25**

[turtlecoin/turtlecoin-rpc-phpTurtleCoin RPC PHP is a PHP wrapper for the TurtleCoin's JSON-RPC interfaces. - turtlecoin/turtlecoin-rpc-phpgithub.com](https://github.com/turtlecoin/turtlecoin-rpc-php)

![screenshot_of_how_wallet_looks_like.PNG](https://miro.medium.com/max/60/0*FwEmcbtapXLywrU3?q=20)

![screenshot_of_how_wallet_looks_like.PNG](https://miro.medium.com/max/1400/0*FwEmcbtapXLywrU3)

**turtle completo —** Hi guys, I have been working on adding the wallet into the local explorer. So far it is going well; however, I will be off for 2 weeks because of some personal business and I won’t be able to have access to computers. I included a screen shot of how the project looks in the git repo.

Sajo has approached me and I am glad that we can work together, because in the following 2 weeks, this project will not just sit there. I will be back soon and I want to encourage everyone to learn how to code and join this wave of massive software engineer demand. We can all contribute to not only the TurtleCoin community, but also to the entire world, solving problems; no matter what your nationality, age, skin color, or gender is. Let’s keep this train up and running forever! **— Sabo (Revolutionary)**

[yumingchangsabodota/turtle-completoturtle local explorer (turtle completo). Contribute to yumingchangsabodota/turtle-completo development by creating an…github.com](https://github.com/yumingchangsabodota/turtle-completo)

![Related image](https://miro.medium.com/max/60/0*EIzJBXYuJ-9HbjF4?q=20)

![Related image](https://miro.medium.com/max/614/0*EIzJBXYuJ-9HbjF4)

**Turtle Tales I —** ‘Turtle tales’ is series of articles that promote core values of Turtlecoin project. The aim of stories, written in layers, is to raise awareness in average world citizen about terms such as ‘open source’, ‘decentralisation’, ‘personal involvement’, ‘reward after true effort’ and to stay in the mind of the reader in the shape of Turtlecoin project. **— Dinkeux**

[Turtle Tales I · Issue #130 · turtlecoin/metaLast night, while listening high-tech minimal - the music of tomorrow and writing some Python code (not far from hello…github.com](https://github.com/turtlecoin/meta/issues/130)

![Image result for spooky turtle](https://miro.medium.com/max/60/0*-WQYIudMWdAj-Cn7.jpg?q=20)

![Image result for spooky turtle](https://miro.medium.com/max/600/0*-WQYIudMWdAj-Cn7.jpg)

**Turtacus —** As people should know by now, Turtacus provides a 1 VS 1 PvP Arena in the colosseum channel. Recently when the payout happens, there has been a lot of “what’s this all about?!” Questions…. So I have now created a new global command “\*info”. This is locked down to me using it because it is global, however when I get the time, I will add this as a private message response. **— Rynem**

[Rynemgar/Gladiator-BotContribute to Rynemgar/Gladiator-Bot development by creating an account on GitHub.www.github.com](https://www.github.com/rynemgar/gladiator-bot)

![]({{ site.baseurl }}/images/0VmNMARSaVqfWRBXJ.png)

**Trtl.rocks** — I’ve been working on some large, mainly architectural, changes to the website. I initially chose to use JSONB to store the node and pool data in the db because I wasn’t quite sure what data would be useful. This decision has not only caused the db to be incredibly large, but also makes it more difficult to add new columns. Now that I think I have a clear idea of where I want to go, I am doing away with the JSONB and storing the data in the appropriate columns. I’ve completed the nodes section and will begin working on the pool data soon. I will also be adding pagination, per page quantity limiting, and fuzzy search to the node and pool tables as well as node fees to the node table. I am hoping to push the new code and have changes live in the next week or two. There will probably be a period where the historical data is missing until I am able to write a script to parse out the data and upload in the new format. **— andrew | trtl.rocks**

[TurtleCoin ExplorerExplore historical and live block, node, pool, and transaction data for TurtleCointrtl.rocks](http://trtl.rocks/)

![Image result for spooky turtle](https://miro.medium.com/max/60/0*5fLo8DfQyUsLiCFd.jpg?q=20)

![Image result for spooky turtle](https://miro.medium.com/max/512/0*5fLo8DfQyUsLiCFd.jpg)

# TRTL Community Bounties!

**100,000 TRTL —** Looking for a “Hunter” turtle design logo. The style of the design can range from the stereotypical “Safari Hunter” look to a badass tribal Hunter turtle. **\-Xaz**

**50,000 TRTL —** 100% guaranteed node restart script. turtlecoid-ha has failed with errors on 3 different systems. i need something i can rely on for a noob to use, and which always works without human intervention. thanks. **— greywolf³˜**

**20,000 TRTL** — Make a Turtle dab emoji **— Sajo8**

**10,000 TRTL** — make a guide on how to mine trtl on an iphone with “XMR Miner”. Must follow format of the existing ‘mine on your phone’ guides. **— Sajo8**

![For Sajo :D](https://miro.medium.com/max/60/0*wNaJh3-d_0KJ4Lt1.jpg?q=20)

![For Sajo :D](https://miro.medium.com/max/1260/0*wNaJh3-d_0KJ4Lt1.jpg)

For Sajo :D

# Community Advertisements

- 0.15 node fee from greywolf³˜ with 2 nodes to choose from: turtlenode.co in Germany; or turtlenode.me in London (both use same port :11898)
- My new public node website is now up with live stats and I’m now running two nodes with TurtleCoind-HA. Node Fees are 5 TRTL and they will be entirely used to fund a TRTL that will be coming soon :) Please come and take a look at [http://turtleland.fun](http://turtleland.fun/) !
- New Pool is looking for miners! We offer PPS + Solo as RewardSystem, Webminer also available! Visit [https://trtl.hackerknowledge.de](https://trtl.hackerknowledge.de/)
- dsmash.turtlenode.online now only charges 5 TRTL per transaction!
- Advertising space now available on [www.turtacus.com](http://www.turtacus.com/) My aim is to fully fund Turtacus from ads on his website. Banners can be provided in any usual banner ads format. Each banner costs 40k trtl for the month.
- Some of you will have seen Scarabey has a new website trtl.turtacus.com Subdomains on Turtacus.com are available if you need or want them.

# TurtleCoin Fork Watch

![]({{ site.baseurl }}/images/0zCznhRq-rvVZMBPI.png)

**Name of your TRTL fork** — AmityCoin

**Github link for your code** — <https://github.com/CalexCore/AmityCoin>

**What is special or new about your network?**

AmityCoin are pioneering the CryptoNight Soft Shell algorithm! One of few ASIC-resistant (also GPU-less and non-pooling) POW coins out there. As a ‘friendly-relations’ coin we’ve a strong focus on social interaction, contribution, and support.

![Image result for spooky turtle](https://miro.medium.com/max/60/0*7TNKc_t7IWSUqruB.jpg?q=20)

![Image result for spooky turtle](https://miro.medium.com/max/560/0*7TNKc_t7IWSUqruB.jpg)

# Shoutouts & Thanks

Rogerrobers — Shout out billiontrtlhomepage.lima-city.de

ChiefCoin — Shoutout for all Twitter Turtles spreading Turtle Love out there ✌

greywolf³˜ — thanks to labaylabay for the reach-out … a good role model for [https://medium.com/@turtlecoin/how-to-be-a-good-turtle-20a427028a18](http://blog.turtlecoin.lol/@turtlecoin/how-to-be-a-good-turtle-20a427028a18)

. — I remember you canti 😘

![Happy Halloween ](https://miro.medium.com/max/60/0*CObMneqUM6ubPNAE.png?q=20)

![Happy Halloween ](https://miro.medium.com/max/1400/0*CObMneqUM6ubPNAE.png)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-oct-30-2018/)_._
