---
layout: "post"
title: "This Week In TurtleCoin (July 21, 2020)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0tDUmt2Y4d26-vXDP.gif"
date: "2020-07-22T03:33:49.089Z"
---

![]({{ site.baseurl }}/images/0tDUmt2Y4d26-vXDP.gif)

Time for TurtleCoin Liftoff! Ledger Nano integration, TRTL V1 ready for launch! GET YOUR MOON BOOTS LETS GOOOO!!!! image credit: teacup

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

TurtleCoin on Ledger Nano!

## TurtleCoin® Ledger Application

**Have a Ledger Nano S or X? Want to use it to keep your TRTL safe? Check out the video… clicky clicky.**

I recently got my hands on a brand new Nano X and the first thing I did was beat it on ground and run over it with my car. After that, I gave it to do the doggo and let him play with it for a bit. After all, if I’m going to store my hard earned TRTL on one of these things, I need to know that it will hold up to abuse.

After I got that testing out of the way, I got to work digging into what it takes to make this bad boy work with TurtleCoin. I admit, the Ledger SDK documentation made everything sound so easy to work through. Let me warn you, it’s not. Looking through headers and source files and trying to keep your head straight while you’re working in C, thinking through how to fit everything important in just 4KB of RAM, and other fun limitations, is not an easy task. In any event, I’ve made some awesome progress in the last 5 days. The Nano is now generating all the necessary keys, exporting public keys, exporting the private view key, and some other basic functionality. I’m still working on completing the necessary pieces and as we all know… slow and steady is the way.

**IBMCD**

<https://github.com/turtlecoin/ledger-app-turtlecoin>

![]({{ site.baseurl }}/images/01oGGnkq2wseaT6Uw.jpg)

image credit: teacup

## TurtleCoin® V0.28 & V1

We’re happy to announce that v0.28.0 is shipping July 22, 2020\. This release upgrades RocksDB to v6.10.2, resolves a few minor bugs that we’ve found along the way, introduces a new TX_EXTRA field just for the pool miner nonces (no pool changes required), and implements a consensus change that requires proof that coinbase (miner rewards) are properly claimed.

> This is also the last release to include turtle-service which means that turtle-service is officially EOL with this release. EOS for turtle-service is scheduled for v1.0.0 which currently planned to be out in time for block 3,000,000.

For those of you looking ahead to what v1.0.0 has to offer, we’ve got quite a few changes stacked up and ready. We’ll be introducing changes to the Proof of Work (PoW) algorithm to help secure the network. The daemon (node) API has been completely overhauled and moves to a more RESTful style implementation versus the json_rpc madness we have today. We’ve also nixed turtle-service, legacy WalletGreen support (this means if you haven’t upgraded your wallet to the new format used by wallet-api and zedwallet, you may want to back up your keys soon). We’re also working on a few other things that will make their way into v1.0.0 in all it’s glory.

Stay tuned for further updates.

T**he TurtleCoin Developers**

[turtlecoin/turtlecoinTurtleCoin is a fun, fast, and easy way to send money to friends and businesses We are a community of people across the…github.com](https://github.com/turtlecoin/turtlecoin)

![]({{ site.baseurl }}/images/0EwAruLKigz3LlDXg.jpg)

## Porting turtlecoin-crypto to FreeBSD

![]({{ site.baseurl }}/images/06w8Cp_hWNNNCFSBJ.jpg)

I ported the turtlecoin cryptography libs over to FreeBSD. They compile on FreeBSD now. Hopefully in the future we can get the turtlecoin-core compiling as well!

**izder456**

[Releases · turtlecoin/turtlecoin-cryptoTurtleCoin: Standalone Cryptography Library. Contribute to turtlecoin/turtlecoin-crypto development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-crypto/releases)

![]({{ site.baseurl }}/images/0XAwUD4_gkWZPw6_M.png)

## Turtle issues

Hebrew translation + issues on mobile when horizontal and slide on IPad (still open)

**@Daniel_Leedan**

[Hebrew translation by Daniel-Leedan · Pull Request #115 · turtlecoin/turtlecoin.lolIssue #111github.com](https://github.com/turtlecoin/turtlecoin.lol/pull/115)

## RTL Support

Add RTL support to the TutleCoin website

**@Daniel_Leedan**

[Add Support for RTL (right-to-left) languages by Daniel-Leedan · Pull Request #112 ·…GitHub is home to over 50 million developers working together to host and review code, manage projects, and build…github.com](https://github.com/turtlecoin/turtlecoin.lol/pull/112)

![]({{ site.baseurl }}/images/0PZwx6hDySN01IPDj.jpg)

image credit: teacup

## TurtlePay® Blockchain Collector

I’m overhauling this bad boy in preparation for v1.0.0 of the TurtleCoin® core software. It’ll store raw blocks, it’ll be faster, it will be stronger, it will be better. I’d say it’s going well but after a week of syncing progress, i’m at block 1.5M. I’ll let you know when it finishes, til then, I think I’ll be working on a few other things.

**IBMCD**

[TurtlePay®TurtlePay®: Fun, Fast, & Easy Crypto Payments. TurtlePay® has 11 repositories available. Follow their code on GitHub.github.com](https://github.com/TurtlePay)

![]({{ site.baseurl }}/images/0Km7ASBg6_byp5wGE.png)

## TurtleTips

After talking with iburnmycd a few months back, I started coding up a little project as a bit of a proof-of-concept for a semi-centralized, non-custodial web wallet — a wallet where _you_ control the spend keys, but a remote server does the hard work of syncing for you. Using this concept, an instance of this wallet, in theory, can sync up in a fraction of the time of conventional methods; as long as the backend is caught up with the network, all the frontend needs to do is play catch-up with whatever inputs and outputs the backend deems relevant.

Recently, I’ve started to rework and revamp my proof-of-concept into a fully-fledged chrome-based extension, with the added capability of being able to send tips to website owners who put their public tipping key up as a TXT record. At the moment, I am finalizing a few things on the front-end, which is basically done, then I’ll be moving onto the backend, where I just need to do a touch of code optimization.

**Canti**

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**Developer — Izder456** for his contributions to getting TRTL going on FreeBSD!

![]({{ site.baseurl }}/images/0Vm4X9gVN9rH9FY8O.jpg)

image credit: teacup

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

MuxDux TurtleCoin Mining Pool — The Patrician’s Choice [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

@turtleMax Shoutout to all the core developers that keep pushing code, slow and steady wins the race! Anonymous F&$k you Dependabot… rebel scum. Some of us have day jobs. You’re not even that good at yours.

## TRTL Dev Afterhours

The afterhours section is a new column we are trying out that aggregates all of the links from **#Dev_OffTopic** for the week so we can share them with you guys.

NewPipe — a free YouTube client  
Welcome to NewPipe, the lightweight YouTube experience for Android  
<https://newpipe.schabi.org/>  
Submitted by RockSteady (TRTL) on Fri, 17 Jul 2020 18:49:00 GMT The Ultimate Oldschool PC Font Pack: FAQ/Docs/ReadMe  
Documentation for the world’s biggest collection of classic text mode fonts, system fonts and BIOS fonts from DOS-era IBM PCs and compatibles  
<https://int10h.org/oldschool-pc-fonts/readme/#history>  
Submitted by RockSteady (TRTL) on Fri, 17 Jul 2020 18:52:49 GMT Beaker Browser  
[https://beakerbrowser.com](https://beakerbrowser.com/)  
Submitted by afterconnery on Mon, 20 Jul 2020 09:21:22 GMT Essays on programming I think about a lot | benkuhn.net  
Computers can be understood • Choose Boring Technology • The Wrong Abstraction • Falsehoods Programmers Believe About Names • The Hiring Post • The Product-Minded Engineer • Write code that is easy to delete, not easy to extend • The Law of Leaky Abstractions • Reflections on software performance • Notes on Distributed Systems for Young Bloods • End-to-End Arguments in System Design  
<https://www.benkuhn.net/progessays/>  
Submitted by RockSteady (TRTL) on Tue, 21 Jul 2020 14:11:00 GMT GitHub — TryGhost/Ghost: The #1 headless Node.js CMS for professional publishing  
The #1 headless Node.js CMS for professional publishing — TryGhost/Ghost  
<https://github.com/TryGhost/Ghost>  
Submitted by ExtraHash on Wed, 22 Jul 2020 00:24:43 GMT Working with Files in Go | DevDungeon  
These practical examples will demonstrate how to work with files including: reading, writing, changing permissions and timestamps, archiving(zipping), compressing, checksum hashing, downloading files over HTTP, buffers, scanners, and links. All examples here use the standard library.  
<https://www.devdungeon.com/content/working-files-go>  
Submitted by ExtraHash on Wed, 22 Jul 2020 00:27:51 GMT

![]({{ site.baseurl }}/images/0KxPS7Uf3jC71blEC.gif)

image credit: teacup

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-21-2020/)_._
