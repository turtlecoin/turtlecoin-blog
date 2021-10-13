---
layout: "post"
title: "This Week In TurtleCoin (September 17, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0S6ZjQ7vyY3g3kYv0.jpg"
date: "2019-09-18T04:46:53.394Z"
---

![]({{ site.baseurl }}/images/0S6ZjQ7vyY3g3kYv0.jpg)

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. [To submit your post, click this link](https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform)

![]({{ site.baseurl }}/images/0QGom95C1IgmVm1vx.jpg)

**violetminer**

I made some great progress on the Nvidia backend for violetminer this week. It’s now working, and hashing at a pretty decent speed. There are still a few more things I need to fix before making a release, however. Firstly, it instantly crashes on Windows 10, due to Windows 10 seemingly reserving about 20% of GPU’s vram. When I limit the memory usage, the performance suffers, so am not sure how best to solve this issue yet.

Secondly, I think I need to alter my code to use streams instead. With the current method, the CPU spins in a loop waiting for the kernel to finish. I believe this is the cause of hashrate being significantly reduced when CPU mining is enabled — the CPU is too busy mining itself to wait for the GPU kernel to finish.

I’ve been working on getting all the automated CI builds working with CUDA, so people don’t have to compile themselves. So far, Linux with both GCC and Clang are working, and so is Mac OSX — but Windows is being a bit of a pain to find the installed cuda toolset. I think I’m getting pretty close to fixing it, however.

Oh — I also need to check the miner works correctly on multiple GPUs. I think I’ve done the programming right, but don’t have multiple GPUs myself, so can’t really test.

I probably also need to add an intensity option for people who don’t want to run their GPUs at max speed.

**Zpalm**

[turtlecoin/violetminerA CPU and NVIDIA miner for TurtleCoin / Chukwa / Argon2id / WrkzCoin. Go here to download the latest release. If you…github.com](https://github.com/turtlecoin/violetminer/tree/nvidia)

[Windows 10 does not let CUDA applications to use all VRAM on (especially secondary) graphics cards.I'm a 3D Graphics artist. I'm using nvidia graphics cards for 3D rendering using CUDA computing. Problem takes place…social.technet.microsoft.com](https://social.technet.microsoft.com/Forums/sharepoint/en-US/15b9654e-5da7-45b7-93de-e8b63faef064/windows-10-does-not-let-cuda-applications-to-use-all-vram-on-especially-secondary-graphics-cards)

![]({{ site.baseurl }}/images/0Ez_osct5sYW_tL4u)

**turtlecoin-wallet-backend-js**

More updates to the JavaScript/TypeScript wallet backend this week. Additions include…

- Auto optimization is now functioning as expected, so your wallet is always ready to send the max amount possible
- Using pre-generated key images to speed up transaction creation
- Improving error messages returned when the daemon fails to process our transaction
- Lots of logging improvements to help out developers debugging

Together with ExtraHash and iburnmycd we’ve also been doing a lot of investigation into some rare issues with wallet syncing, and wallet transacting. A ton of bugs have been found and fixed, so hopefully we’ll see a lot less of those weird issues when utilising the js backend or the blockchain cache.

It looks like the library is getting a fair bit of usage in different projects — I’m seeing the library getting downloaded over 130 times a week, and is now being included by at least 24 different projects on GitHub!

As a reminder to folks who may not know what the library does, it lets you run a full client side wallet entirely in JavaScript, with no other processes needed. This allows for a lot of options on how to use the wallet, given how versatile JavaScript is. It also allows a much more seamless and integrated experience for the users, as it does not require a flaky RPC API interface to be used.

I have a few more interesting features I hope to get added in the next couple of weeks, so stay tuned ;o

**Zpalm**

[turtlecoin/turtlecoin-wallet-backend-jsMaster Build Status NPM Github https://github.com/turtlecoin/turtlecoin-wallet-backend-js Provides an interface to the…github.com](https://github.com/turtlecoin/turtlecoin-wallet-backend-js)

**Client Side Web Wallet**

Has been a slow two weeks, but wallet creation and storing them client side (locally on the device) works now. Next up will be to to create a simple login page and dashboard displaying transactions and balance. I will be pushing code to Github soon.

**fexra**

![]({{ site.baseurl }}/images/0JMNSEjtxywBOt9PA.jpg)

**BLOC GUI MINER**

BLOC GUI Miner is a beautiful, easy to use, Graphical User interface for mining multiple cryptocurrencies based on cryptonote. The BLOC GUI Miner is easy to use and makes you getting started with mining cryptocurrency on Windows, MacOS and Linux in no time.

It is aimed at getting people that have never tried mining before with a focus on accessibility, security and simplicity.

BLOC GUI Miner support two very popular miner backends: xmr-stak and xmrig

BLOC GUI Miner comes with XMR-STAK 2.10.7 and XMRIG 3.1.1 already built-in, including configuration files for CPU and GPU mining in most of the cases.

What’s new in v1.1.1 ?  
A lot of updates in this release. BLOC GUI Miner now support following crypto-currencies:

- BLOC.MONEY (BLOC)
- TurtleCoin (TRTL) (New Chukwa Algorithm supported)
- RYO (RYO)
- Haven (XHV)
- Monero (XMR)
- Adding support to mine cryptocurrency: Monero (XMR), Haven (XHV), RYO (RYO)
- XMR-STAK.log is now created while using XMR-STAK miner with BLOC GUI Miner
- Updated miner setting to support the latest version of XMR-STAK v2.10.7
- Updated miner setting to support the latest version of XMRIG v3.1.1
- TurtleCoin now changed to Chukwa CPU mining algorithm
- Fixed a bug that changed the XMR-STAK CPU config when changing thread count
- Fixed draggable windows on macOS
- Added new cryptunit widget built-in
- Fixed Coinggecko stats for each supported currency
- Added new box with image and link on the left custom for each coin
- 1st pool now automatically selected on 1st run
- Added simple menu selector in the pool settings. Mining from CPU or GPU. (Corresponding port will be automatically selected on the mining pool.)
- Fixed infinite GUI errors coming from electron
- Added price usd for informations section
- Updated XMR-STAK exact config file to latest 2.10.7
- Added an experimental functionality to recover when xmr-stak stats stop to restart the miner

Download link: <https://github.com/furiousteam/BLOC-GUI-Miner/releases/tag/v1.1.1>

More updates coming soon.

Thank you for your feedback. That’s what keep us alive

**furiousteam**

[furiousteam/BLOC-GUI-MinerYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/furiousteam/BLOC-GUI-Miner/releases/tag/v1.1.1)

![]({{ site.baseurl }}/images/0VdlShRRTv4WKzXyP)

**Contribute your Miner stats for Chukwa**

I put up a simple Google Form to gather stats about mining hardware/software combos. Contribute your stats for others to have a reference. The form is pinned in the #mining channel on discord for future reference as well.

_Image by Лечение Наркомании from Pixabay_

**SoreGums**

[chukwa-hashing-statsClean Results Type,Hashes/sec,KH/s,MH/s,Device,Miner,Params or Notes,Operating System,Who?,Red, Green, Blue or Other…docs.google.com](https://docs.google.com/spreadsheets/d/1vY7l3KSTk5oUL8mp74Cxjl-EdBLC-jjpDpRGiiNXJGY/)

[Discord - Free voice and text chat for gamersStep up your game with a modern voice & text chat app. Crystal clear voice, multiple server and channel support, mobile…discordapp.com](https://discordapp.com/channels/388915017187328002/410271688748695562/617848232726364170)

![]({{ site.baseurl }}/images/0JJY-BPgQfW81CKxl)

**NinjaRig on Android via Termux**

Updated the guide for running NinjaRig (XMRig) on Android via Termux if you’re into that kind of thing :)

Thanks to Haifa Bogdan Adnan for NinjaRig it has been a bit of a hit with the move to chuckwa PoW hashing algorithm. As mentioned in the guide had to remove a part of the code to make it work on Android, hence why it pulls from my repo, which is kept up to date with upstream.

**SoreGums**

[Mining with Termux · TurtleCoin DocsDownload Termux from the Play Store or fromF-droid. Upon downloading and installing, open the app. Run pkg upgrade -y…docs.turtlecoin.lol](https://docs.turtlecoin.lol/guides/mining/using-termux)

[turtlecoin/ninjarigIn order to support development, this miner has 1-5% configurable dev fee - 1-5 minutes from 100 minutes it will mine…github.com](https://github.com/turtlecoin/ninjarig)

**Blockfolio Signa**l

TurtleCoin Updates via Blockfolio Signal

A call-out to members in the community and gaining your support by contacting Blockfolio and requesting they add us as a project to Signal: [support@blockfolio.com](mailto:supprt@blockfolio.com)

Rock says it best “_… if more people ask they’ll feel the collective hands on hips demanding turtle updates_”

**404_Not_Found**

[Join Blockfolio SignalBlockfolio Signal is a first-of-its-kind communications platform built exclusively for token teams to connect and…blockfolio.com](https://blockfolio.com/signal/apply)

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**DJ** — Teacup, Zerouan, rogerrobers, zpalmtree, muf, bratovenhurt

**Developer** — Bogdanadnan

**Contributor** — June, sajo8, farhod, PStarSR

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

## Pay With TRTL

In Discord we have a channel called #Merchandise where people can post things you can buy with TRTL. To view items for sale, check the pinned posts in that channel. These are a few of the items from this week.

**All items in our shop:**

- ‘Small NEOS Voyager Overshoes’ by Dustin Thewind | turtleland.fun#1350  
  ID: #124437
- ‘Xbox 360 120GB with 10 Games (+1 PS3 Game)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #196185
- ‘Alan Wake Collector’s edition (Xbox 360)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #196847
- ‘Diablo 3 + ROS Collectors edition’ by Dustin Thewind | turtleland.fun#1350  
  ID: #362655
- ‘Lot of Zombie Books (Walking Dead Mostly)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #654412
- ‘Lot of 15 PC games (Most of them are redeemed on steam and will not be usable online)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #654681
- ‘Lot of Xbox One Games (12 Games)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #702770
- ‘eBook’ by DroppingThePacketsHard²#4751  
  ID: #726088
- ‘SC2 Collector Editions (Main Game + 2 Expansions)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #750847
- ‘Gigabyte X570 AORUS MASTE’ by Elkim#7747  
  ID: #753245
- ‘Lot of BluRay discs (Movies, Series)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #858719
- ‘ASUS X570 STRIX GAMING-F’ by Elkim#7747  
  ID: #862191
- ‘Final Fantasy XIII2 Collector’s Edition (PS3)’ by Dustin Thewind | turtleland.fun#1350  
  ID: #867107
- ‘Lot of 4 Nintendo Gamecub Games.’ by Dustin Thewind | turtleland.fun#1350  
  ID: #957775
- ‘Lot of 5 Game Boy Games’ by Dustin Thewind | turtleland.fun#1350  
  ID: #983802
- ‘ASUS X370 ROG CROSSHAIR VI EXTREME’ by Elkim#7747  
  ID: #010771
- ‘Sega Dreamcast with 3 original games’ by Dustin Thewind | turtleland.fun#1350  
  ID: #081097
- ‘Wacom Bamboo Tab MTE-450’ by Dustin Thewind | turtleland.fun#1350  
  ID: #001659
- ‘Halo Reach Collector Edition for Xbox 360’ by Dustin Thewind | turtleland.fun#1350  
  ID: #032088
- ‘Logitech MX Master 910–004337 5 Buttons 1 x Wheel USB Bluetooth Wireless 1600 dp’ by Dustin Thewind | turtleland.fun#1350  
  ID: #027270
- Provided by fipsi#0789 and DroppingThePacketsHard²#4751

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

![]({{ site.baseurl }}/images/0T4uRTjJx1o3DQeyG)

“WaitingForAnOpenCaseVegaRig” by HashBrownie

This is a 4 vega56 Rig — 3 Radeon Gigabyte vega 56 and 1 Asus Strig Vega 56..Currently mining as is (waiting for an actual open mining rig case to show up) on stock settings  
No secrets at all.. got a good room temp of 18–20 C and ninjarig is kickass with AMD GPUs  
**HashBrownie** 240 KH/s

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- Support the only Duck-Themed TurtleCoin Mining Pool <https://trtl.muxdux.com/>
- Hi fellow turtles :) TurtleAds just launched! On TurtleAds you can advertise you node, pool or any other service using Turtlecoin. If you are a website owner, feel free to include your script and start earning Turtlecoin immediately. Make sure to sign up today and start earning or advertising. Regards, fipsi#0789 :) <https://turtleads.org/>

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- greywolf thanks to those that were helpful in the past year with issues with my public node. but the latest update killed me and I can’t figure it out so I pulled the node down. thanks again to all those that did help before and I wish the rest of you good luck with public nodes still running, going forward.
- @MrLahaye Thanks @Rocksteady for buying my old NES on the #merchandise channel. My second item sale using TurtleCoin. :D Who’s gonna be my next buyer?
- greywolf a big thanks to zpalmtree for helping me get my public node back up, and also to iburnmycd for fixing my github errors in updating the nodes list.
- wll1rah bogdanadnan, thanks for the great ninjarig miner and the help that you have provided in getting to work with mali GPU with OpenCL.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-september-17-2019/)_._
