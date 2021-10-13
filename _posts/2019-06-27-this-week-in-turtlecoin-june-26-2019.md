---
layout: "post"
title: "This Week In TurtleCoin (June 26, 2019)"
description: "As I mentioned last week, I was working on upgrading turtle-service/zedwallet wallets to the WalletBackend/zedwallet-beta format. This is now complete, and I went ahead and implemented the…"
image: "{{ site.baseurl }}/images/0RUEGtTIeoHn9PEZ7.gif"
date: "2019-06-27T03:44:28.930Z"
---

## Developer Updates

![]({{ site.baseurl }}/images/0RUEGtTIeoHn9PEZ7.gif)

**Wallet format upgrading**

**Wallet format upgrading**

As I mentioned last week, I was working on upgrading turtle-service/zedwallet wallets to the WalletBackend/zedwallet-beta format. This is now complete, and I went ahead and implemented the transparent upgrade feature.

Once the PR is merged, you can go ahead and open an old style wallet in zedwallet-beta or wallet-api and it will upgrade it, and retain all syncing progress, transaction history, and so on.

This should make it a lot easier for new GUI wallets or services to upgrade without having to bother reimporting their wallets.

**Zpalm**

**TonChan**

I’ll probably be releasing a new TonChan version in a few days. It’s nothing major, but there’s some wallet sync speed improvements, 64 bit support, and a few bugfixes. I’m pretty happy with where it’s at, it works pretty nicely aside from somewhat slow syncing, the only real feature it’s lacking is optimizing.

However, this feature is present in the new version of the wallet backend it’s using, so it would be pretty trivial to add a manual optimize, but it also has an auto optimize feature, which is enabled by default.

Haven’t really had any time to fuck around with the C++ backend to see if we can get faster syncing on mobile I’m afraid. Kinda a large time investment where the only positive outcome is faster syncing speed.. :/

Remember if you’re importing a wallet from desktop, check the FAQ screen for a few tips on how to greatly increase your sync speed.

**Zpalm**

![]({{ site.baseurl }}/images/07jCfFk61JaVAPSrt.gif)

**WalletBackend**

**WalletBackend**

Fixed a rare bug in WalletBackend which would cause about 1 in 256 transactions with a payment ID to be incorrectly scanned. If you were having balance discrepancies running wallet-api, please update your daemon to the dev branch and resync to see if it fixes it.

**Zpalm**

![]({{ site.baseurl }}/images/0aSiVA_9zmhPJCK-H)

**turtlecoin-wallet-backend**

**turtlecoin-wallet-backend**

Small update to the js backend to fix the config being static — this would cause issues when the library was initialized multiple times with different coins, for example, if you were creating a multi-coin wallet. It should now work perfectly with multiple coins at once.  
Thanks to fipsi for reporting this so I could get it fixed.

**Zpalm**

## Rig Of The Week

**Rig3 by Greywolf** _(all stock settings) just over 19K H/s_

![]({{ site.baseurl }}/images/0M3IK7Oegfr8rwgWv)

![]({{ site.baseurl }}/images/0U8rY3zUn5SO76qS-)

![]({{ site.baseurl }}/images/0go5hk65VvZe310qj)

it is an open air frame i constructed with 1/2" angle aluminum bars, and some self-tapping screws to hold it together. it sits on a 1" thick rectangular piece of smooth plywood. the frame has five (5), 2–1/2" wide slats of wood, to support the mobo and PSU. i positioned a 6" long angle aluminum bar mounted to the frame in the rear, to support the GPUs. the components are EVGA 500W PSU, GIGABYTE GA-AB350-Gaming 3 mobo, AMD Ryzen 3 1200 quad core CPU, Patriot Viper Elite Series DDR4 8GB (2x4GB) 2666MHz PC4–21300 RAM, Windows 10 Pro on a 120GB SSD, with a 64GB SSD to store data and installed programs, AMD RX Vega 56 and two (2) AMD RX550 GPU’s, with a standard PC speaker and an on/off switch wired to the mobo jumpers, a single-dongle Logitech wireless keyboard and mouse, and a USB 3.0 extension cable from the rear panel to the front of the rig for easy access.

i don’t have any secrets, i run everything stock, and when stuff breaks, i ask for help from the best community in the crypotosphere, found in the Discord TRTL Network server

greywolf — i’ve been with the community a few months past a year

## Shoutouts & Thanks

Rock — shouts out to zpalm who wrote the entire roundup this week.

Rock — shouts out to everyone who participated in last week’s DnD sesh with the TRTL crew. It was really fun and I’m looking forward to continuing the campaign this weekend :D

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-june-26-2019/)_._
