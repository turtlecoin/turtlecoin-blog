---
layout: "post"
title: "This Week In TurtleCoin (July 29, 2020)"
description: "This week we put the pedal to the metal and knocked out our biggest developer bounty we have ever had, in the name of TurtleCoin adoption and security of your coins! You are going to love it! Keep…"
image: "{{ site.baseurl }}/images/0bbJMGQOQawaCgUmJ.png"
date: "2020-07-30T03:06:51.905Z"
---

![]({{ site.baseurl }}/images/0bbJMGQOQawaCgUmJ.png)

This week we put the pedal to the metal and knocked out our biggest developer bounty we have ever had, in the name of TurtleCoin adoption and security of your coins! You are going to love it! Keep reading

> Like the sound of bounties? Have skills? Visit our **#bounties** channel for your chance to get paid and earn a limited edition pink TurtleCoin Developer role in Discord @ chat.turtlecoin.lol

![]({{ site.baseurl }}/images/0SfuHjsNKsegKXldH.png)

Image courtesy of [Teacup](https://github.com/turtlecoin/teacup)

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

![Octocat Ninja Turtle by Danilo Quilaton on Dribbble](https://miro.medium.com/proxy/0*4K6SvP4M3Sfp6mE5)

[Octocat Ninja Turtle by Danilo Quilaton on Dribbble](https://dribbble.com/shots/2110418-Octocat-Ninja-Turtle)

## Github tip bot

Recently I have been working on a tip bot for Github which allows users to tip each other by commenting on issues. It is triggered by a command that discord users will be familiar with to send a tip, for example:

> **.tip 3.50 @username**

If the receiving user doesn’t have a tips account yet, any tips sent to that user still get processed and are available to them when they create an account. To create an account a user simply has to sign in to the react web app with Github auth and they’re all set.

It is also possible to set an optional time-out for unclaimed tips(tips sent to users who have not activated an account yet), if an unclaimed tip expires, the original sender is refunded.

**If you’d like to help test the bot ping me on discord :)**

**zoidbergZA**

![]({{ site.baseurl }}/images/0pVrE84b5a02RHCJU.png)

Image courtesy of [Teacup](https://github.com/turtlecoin/teacup)

> **New Translations for TurtleCoin website!**  
> Chinese, French and Turkish  
> _mason2woods, RocksteadyTC, KontViper_
>
> Submit a translation in your language here: <https://github.com/turtlecoin/turtlecoin.lol>

<https://github.com/turtlecoin/turtlecoin.lol/pull/113>  
<https://github.com/turtlecoin/turtlecoin.lol/pull/110>  
<https://github.com/turtlecoin/turtlecoin.lol/issues/120>

## TurtleCoin® Ledger Wallet

Over the last week I was able to get Ring Signatures working on the Ledger Nano S. After doing that, checking ring signatures was easy. I’ve also exposed a few other crypto fundamentals that are used in wallet management in the event that we absolutely have no other choice but to use the crypto functions on the device (it’s not a fast as a host device — the Nano S sports a < 100Mhz CPU). Needless to say, as you can see, this the application on the ledger is pretty much all but “done” (knowing full well that development is never done).

I’ve set up the CI/CD pipeline for the project with GitHub actions including Unit Tests against the Nano S emulator, making it very easy to tell when something isn’t working. I used the same test script but pointed at a real Ledger Nano S to create the video you see here.

There are a number of tools that I’m also building out for talking to the application when it’s running on the Ledger. See the rest of my updates for more :)

**IBMCD**

[turtlecoin/ledger-app-turtlecoinThis app is a boilerplate for a Nano S/X app. It does very little, and just expose a minimal API (get_app_config…github.com](https://github.com/turtlecoin/ledger-app-turtlecoin/)

![]({{ site.baseurl }}/images/0HVgzdEeb3r2gFZxX.png)

## TurtleCoind® Crypto Library

Just rolled a new major version of the TurtleCoin crypto library v5.0.0\. A few minor bug fixes are included but the biggest change is that the TS/CommonJS exports are all async now, which will pave the way for going down into the actual C++ code to make them asynchronous. As a bonus, the library now includes the code for Chukwa v2 as well as a few utility functions to make it easier to handle any other Argon2id variants.

**IBMCD**

[Release v5.0.0 · turtlecoin/turtlecoin-cryptoYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/turtlecoin-crypto/releases/latest)

![]({{ site.baseurl }}/images/01KWUGKTRb1iFtRKh.gif)

Image courtesy of [Teacup](https://github.com/turtlecoin/teacup)

## TurtleCoin® Utilities Library

With the recent changes to TurtleCoin-crypto going full async, there were a number of changes that had to take place in this library as well. Most of the updates taking place in the library are related to that and as soon as I’m 100% comfortable it’s ready, I’ll bundle up the release. This next release will also be a major version change as the async changes require a bit of tweaks to downstream code and thus broke the API expectations.

In addition, I’ve added a small export that provides the necessary functions to talk to a Ledger Hardware device running the TurtleCoin® Ledger Wallet application. You supply the transport mechanism (HID, USB, BLE, etc.) and the class does the rest. Every command supported by the application today can be handled via the class added to the library. Looking forward to start hooking it up to things wallets like Proton.

**IBMCD**

[TurtleCoin-UtilsThis package contains code that wraps turtlecoin-crypto primitives into an easier to use interface. This includes the…utils.turtlecoin.dev](https://utils.turtlecoin.dev/)

![https://i.imgur.com/lVQY2Nt.png](https://miro.medium.com/max/60/0*YBtPxB_m4wx6o3FP.png?q=20)

![https://i.imgur.com/lVQY2Nt.png](https://miro.medium.com/max/1400/0*YBtPxB_m4wx6o3FP.png)

## TurtleCoin® Block Explorer

Did a couple of small updates to the explorer over the weekend in preparation for the network upgrade at block v0.28.0\. It’s subtle, and it’s not always there, but you’ll get it when you see it.

Also went through and updated the TurtleCoin® Utilities package deployed with the explorer as there’s some big things coming to the blockchain api that’ll open up a lot more data for the explorer.

**IBMCD**

[TurtleCoin Block ExplorerBlock Explorer for the TurtleCoin network that is a fun, fast, and easy way to send money to friends and businesses.explorer.turtlecoin.lol](https://explorer.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0pSoIi8go4hjnjZca.jpg)

Image courtesy of [Teacup](https://github.com/turtlecoin/teacup)

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

This **Good First Issue** comes from Zedwallet developer Zpalmtree who requests a brave dev newbie who can add two commands to Zedwallet. This GFI is cool because it gets you both a **Developer** and a **Core Contributor** role in the chat!

- `list_fusions` command for zedwallet
- `rewind` command for zedwallet, the same way as it is implemented in[ turtlecoin wallet backend js](https://github.com/turtlecoin/turtlecoin-wallet-backend-js)

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

**MuxDux TurtleCoin Mining Pool — The Patrician’s Choice** [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## Shoutouts & Thanks

_This is the place to mention someone in the community who has done something nice or deserves recognition._

**Dreday000** Shout to the devs, working hard :) **@turtleMax** Shoutout to all the core developers that keep pushing code, slow and steady wins the race! **Anonymous** F&$k you Dependabot… rebel scum. Some of us have day jobs. You’re not even that good at yours. **@Daniel_Leedan** I just want to say thank you to all the members of the community who patiently helped me with the new computer specifications and explained to me lots of technical issues. I learned a lot from you. I could not do it without you. Thanks Turtles.

## TRTL Dev Afterhours

_The afterhours section is a new column we are trying out that aggregates all of the links from #Dev_OffTopic for the week so we can share them with you guys._

**Amazon Ion**  
Amazon Ion is a richly-typed, self-describing, hierarchical data serialization format offering interchangeable binary and text representations. Ion was built to address rapid development, decoupling, and efficiency challenges faced every day while engineering large-scale, service-oriented architectures. Ion has been addressing these challenges within Amazon for nearly a decade, and we believe others will benefit as well.  
<https://amzn.github.io/ion-docs/>  
Submitted by RockSteady (TRTL) on Wed, 22 Jul 2020 23:41:37 GMT **MessagePack: It’s like JSON. but fast and small.**  
<https://msgpack.org/>  
Submitted by ExtraHash on Thu, 23 Jul 2020 03:28:02 GMT <https://github.com/turtlecoin/turtlecoin-utils/blob/master/src/Types/PortableStorage.ts>  
Submitted by iburnmycd on Thu, 23 Jul 2020 03:55:14 GMT **A half-hour to learn Rust — fasterthanli.me**  
In order to increase fluency in a programming language, one has to read a lot of it.  
But how can you read a lot of it if you don’t know what it means? In this article, instead o…  
<https://fasterthanli.me/articles/a-half-hour-to-learn-rust>  
Submitted by RockSteady (TRTL) on Thu, 23 Jul 2020 06:52:45 GMT **Linus builds Linus new PC! — YouTube**  
Check out Storyblocks Video at <https://www.storyblocks.com/linustechtips> Linus has built a new PC for himself, and now Linus is going to replicate it as best…  
<https://youtu.be/Kua9cY8q_EI>  
Submitted by rashedmyt on Thu, 23 Jul 2020 17:08:24 GMT **NISTs Post-Quantum Cryptography Program Enters Selection Round | NIST**  
<https://www.nist.gov/news-events/news/2020/07/nists-post-quantum-cryptography-program-enters-selection-round>  
Submitted by RockSteady (TRTL) on Fri, 24 Jul 2020 17:56:13 GMT **X570 AORUS ELITE (rev. 1.0) | Motherboard — GIGABYTE U.K.**  
AMD X570 AORUS Motherboard with 12+2 Phases Digital VRM with DrMOS, Advanced Thermal Design with Enlarge Heatsink, Dual PCIe 4.0 M.2 with Single Thermal Gua…  
<https://www.gigabyte.com/uk/Motherboard/X570-AORUS-ELITE-rev-10/sp#sp>  
Submitted by zpalmtree on Sun, 26 Jul 2020 01:40:56 GMT **New Meow attack** has deleted almost 4,000 unsecured databases  
Dozens of unsecured databases exposed on the public web are the target of an automated ‘meow’ attack that wipes data without any explanation.  
<https://www.bleepingcomputer.com/news/security/new-meow-attack-has-deleted-almost-4-000-unsecured-databases/>  
Submitted by madk on Sun, 26 Jul 2020 22:28:58 GMT <https://github.com/satorigold/SatoriCoin/issues/1#issue-666639654>  
Submitted by Crappyrules on Mon, 27 Jul 2020 23:10:43 GMT **@zondax/zemu — npm**  
Zemu Testing Framework  
<https://www.npmjs.com/package/@zondax/zemu>  
Submitted by iburnmycd on Tue, 28 Jul 2020 02:52:49 GMT **LG Monitor: Onscreen Control & Splitscreen — YouTube**  
Multitasken met meerdere programmas overzichtelijk naast elkaar.  
<https://www.youtube.com/watch?v=Z-jqqQdRRzI>  
Submitted by Daniel_Leedan on Tue, 28 Jul 2020 10:56:30 GMT <https://twitter.com/github/status/1288161164250083329?s=19>  
Submitted by rashedmyt on Wed, 29 Jul 2020 01:23:12 GMT **Courses TurtleEDU**  
<https://edu.turtlecoin.lol/courses/>  
Submitted by rashedmyt on Wed, 29 Jul 2020 04:09:55 GMT **Courses TurtleEDU**  
<https://edu.turtlecoin.lol/courses/>  
Submitted by Daniel_Leedan on Wed, 29 Jul 2020 04:11:53 GMT **DisplayPort — Wikipedia**  
<https://en.wikipedia.org/wiki/DisplayPort>  
Submitted by zoidbergZA on Wed, 29 Jul 2020 14:43:50 GMT

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-29-2020/)_._
