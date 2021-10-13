---
layout: "post"
title: "This Week In TurtleCoin (August 20, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0gIMBxrh-jN8UQ4Ct.gif"
date: "2019-08-21T04:07:57.243Z"
---

![]({{ site.baseurl }}/images/0gIMBxrh-jN8UQ4Ct.gif)

[_We’re forking ready to get this show on the road!_](https://blog.turtlecoin.lol/archives/the-quest-for-decentralized-proof-of-work/)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._ [_To submit your post, click this link_](https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform)

![]({{ site.baseurl }}/images/0Um-7GytQayU1Xt7S)

Proton Wallet

**Proton Wallet**

Hey guys, I’ve just released the newest version of Proton Wallet, my wallet client for TurtleCoin. As always, you can download it at the link below. This wallet rewrites a ton of the logic powering the wallet and makes the entire thing leaner, meaner, and more modular. There’s also a few new features: closing to tray being toggleable in settings, a lock button in the navbar, as well as an auto-lock feature which locks your wallet with a password after 15 minutes of inactivity. Check out the changelog on the releases page for more details (and download the latest release!) Hope you guys are enjoying the wallet

**ExtraHash**

[turtlecoin/turtle-wallet-protonYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…getproton.org](https://getproton.org/)

![]({{ site.baseurl }}/images/0sUsiHpJH31vcjkBn.png)

TurtlePay

**TurtlePay**

After much consideration, I’m working on adding the ability for developers to supply their own view key and address when creating a new payment request. In doing so, TurtlePay will continue to monitor the TurtleCoin blockchain for incoming funds and fire alerts as it does now; however, it will never actually have access to the funds as the user will send funds directly to the specified wallet. This provides another avenue for payment processing that other projects do not have.

**IBMCD**

[TurtlePayTurtlePay™ is a payment processing service that is designed to help developers integrate TurtleCoin™ payments into…turtlepay.io](https://turtlepay.io/)

![]({{ site.baseurl }}/images/06LYnO9nVwwNd5fKl.jpg)

violetminer

**violetminer**

My miner has come a long way since the last roundup post. It is fully functional now, and has had lots of optimizations implemented for the different intrinsics available on different x86–64 CPUs. From my tests, it hashes just as well as trtlrig or better!

Today I’m working on adding some ARM optimizations, which I think trtlrig doesn’t have yet, so make sure to check out the hashrate after I get those in if you’re an SBC fan :)

Aside from the hashing speed improvements, there were lots of improvements to how the miner communicates with the pool. Still lots more to make the miner easier to use though, I need to improve the hashrate reporting, and add some interactive commands. Hopefully I can get that done before the fork date arrives!

**Zpalm**

[turtlecoin/violetminerA CPU miner for Argon2i, Argon2d, and Argon2id. Go here to download the latest release. If you prefer to compile…github.com](https://github.com/turtlecoin/violetminer)

![]({{ site.baseurl }}/images/0uaXO9ecxSz33wDsj.gif)

Moving on up! Thanks to all the community members who took new roles in the community this week!

## Moving Up!

_It’s always good to be recognized! These are the people who gained new roles in the community this week!_

**Sajo8, PstarSR, DroppingThePacketsHard, Farhod — Contributor**

Great job, y’all!

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- **Use matches property in ApiDispatcher regex #862**  
  Some calls in the [ApiDispatcher](https://github.com/turtlecoin/turtlecoin/blob/development/src/walletapi/ApiDispatcher.cpp) use a regex, for example, `getTransactionDetails`. They then extract the query parameters. We could instead extract `hashStr` using the `matches` property on the `req` object, by adding a capture group to the hash regex.  
  <https://github.com/turtlecoin/turtlecoin/issues/862>
- **Remove no longer relevant asserts #811**  
  Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.  
  <https://github.com/turtlecoin/turtlecoin/issues/811>
- **Daemon+WalletBackend timestamp adjustments #704**  
  The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away).  
  <https://github.com/turtlecoin/turtlecoin/issues/704>

![]({{ site.baseurl }}/images/0DJT9XSBIQOnUprT2.gif)

## Pay With TRTL

_In the Discord we have a channel called #Merchandise where people can post things you can buy with TRTL. To view items for sale, check the pinned posts in that channel. These are a few of the items from this week._

![]({{ site.baseurl }}/images/0QjonaUdex5W0_5r9)

**List of all items**  
_Type -item in the #merchandise channel in Discord to view more details for an item_

- ‘Small NEOS Voyager Overshoes’ by Dustin Thewind | turtleland.fun#1350  
  ID: #124437
- ‘Alan Wake Collector’s edition (Xbox 360)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #196847
- ‘Orignal NES in Box’ by Dustin Thewind | turtleland.fun#1350  
  ID: #496247
- ‘Lot of bluray tv series’ by Dustin Thewind | turtleland.fun#1350  
  ID: #514474
- ‘eBook’ by DroppingThePacketsHard²#4751  
  ID: #726088
- ‘-Gigabyte X570 AORUS MASTE’ by Elkim#7747  
  ID: #753245
- ‘-ASUS X570 STRIX GAMING-F’ by Elkim#7747  
  ID: #862191
- ‘ Xbox 360 Slim (120GB) + 9 Games’ by Dustin Thewind | turtleland.fun#1350  
  ID: #863214
- ‘Final Fantasy XIII2 Collector’s Edition (PS3)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #867107
- ‘Lot of 4 Nintendo Gamecub Games.’ by Dustin Thewind | turtleland.fun#1350  
  ID: #957775
- ‘- Hand Forged Damascus Hunting Knife ‘ by Ftwjason#9933  
  ID: #958971
- ‘Lot of 5 Game Boy Games’ by Dustin Thewind | turtleland.fun#1350  
  ID: #983802
- ‘Lot of bluray movies’ by Dustin Thewind | turtleland.fun#1350  
  ID: #994017
- ‘ASUS X370 ROG CROSSHAIR VI EXTREME’ by Elkim#7747  
  ID: #010771

**_This MerchandiseBot item listing provided by fipsi#0789 and DroppingThePacketsHard²#4751_**

![]({{ site.baseurl }}/images/0rgOBlHj3wF7oM8BA.gif)

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

- Hi Guys, it is with great regret that I announce that the turtlepool.space mining pool will be closing. I have been here since day one, and it’s been fantastic to see the community grow and develop from 20 people meming, and network forks every hour, to the 15,000 members there are now. I will still keep other services I run going, such as the tag/star discord bot, and my public node. For more details, please see the attached link. <http://turtlepool.space/pool_closure.html>
- I used to have one of the higher fees, not anymore muahaha! Still going, even better uptime thanks to the crew here! [http://turtle.japakar.com](http://turtle.japakar.com/)
- List of nodes and pools! <https://trtl.nodes.pub/>

![]({{ site.baseurl }}/images/0pRN2b71lje7Jvna3.gif)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- Rogerrobers Shout out Leo congrats on the baby!!
- JAPAKAR DUH di doy doy Thanks to all around here still going strong! I havent been able to get online much at all but looking forward to the 1.8 block!
- Rock shouts out to the usual suspects keeping the karaoke channel going :D, and to the nerds in Abylon who keep their d20’s rolling strong

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-august-20-2019/)_._
