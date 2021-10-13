---
layout: "post"
title: "Weekend Roundup (Apr 14, 2018)"
description: "EVERYTHING-SINCE-LAST-TIME-TILL-NOW EDITION"
image: "{{ site.baseurl }}/images/0CeM-wa5u8MuWkzIS.jpg"
date: "2018-04-15T16:57:09.059Z"
---

## EVERYTHING-SINCE-LAST-TIME-TILL-NOW EDITION

![]({{ site.baseurl }}/images/0CeM-wa5u8MuWkzIS.jpg)

We told you we were going to do it. We’ll do it again too.

[The chat grew to 9,750 Turtles this week! Join our chat! ](http://chat.turtlecoin.lol/)It’s been a long minute since the last update. So much has happened between now and three weeks ago, but luckily the mad scramble to a new algorithm has paid off and we are happily humming along at 8.51MH.

## Our New Hashing Algorithm

I’ll link the article below, but to sum it up, we were alerted a few weeks ago to credible reports of ASIC miners being available for purchase. Sticking by our commitment to keeping mining ASIC-free and competitive, we pivoted to a new algorithm that you may be familiar with: Cryptonight Lite Variant 1

[What is the Deal with ASIC?While we talk about algorithm changes, I wanted to give some detail to TurtleCoin users about what’s happening now…medium.com](https://medium.com/@turtlecoin/what-is-the-deal-with-asic-d22b86510c6)

The transition is a two stage hashing algorithm change that is currently beginning phase two. Phase one gets us out of the way of ASIC for now, and incidentally NiceHash as well, for the moment. Phase two gets us a more suitable long term hashing algorithm to carry us into 2019.

## TRTL-Stak, lol

During the transition to our stage 1 algorithm change, we were attacked repeatedly, which rushed the transition to the new algorithm. When we are making these changes, it requires the participation and cooperation of everyone else, which we almost didn’t have as a result of the attacks pushing the transition date ahead by 6 days.

Initially, we wanted to have at least the big two covered, XMR-stak and XMRig, which both voiced support for our algo change. The schedule moving forward made this difficult, as XMRig was the first to swap but most of our miners still preferring to use other software. We had to rush out an adapted version of xmr-stak that we affectionately called TRTL-stak.

As cool as it is having a miner named after us, when XMR-stak is released officially we will be retiring TRTL-stak in favor of the continuously supported XMR-stak. In the mean time, it is fine to use.

[turtlecoin/trtl-staktrtl-stak - Unified All-in-one Cryptonote minergithub.com](https://github.com/turtlecoin/trtl-stak)

## Bet your #MCM doesn’t have 5 GUI wallets

There’s a new tag in the chat now to summon a link to all of the graphical wallets currently available. Even with one or two of them currently retired, we still have 5 active GUI wallets currently, which just screams one thing… OPULENCE.

Download one of our wallets today, and put your hands on a piece of organic, fair-trade, handmade, bespoke, poverty-repellent software. Here’s a quick link to all of our GUI projects

**#1 This wallet is written in Golang. Supports Win/Mac/Linux**

![]({{ site.baseurl }}/images/0FsKKYYTm7uuafUGL.png)

[turtlecoin/turtle-wallet-goturtle-wallet-go - A universal gui wallet for TurtleCoingithub.com](https://github.com/turtlecoin/turtle-wallet-go)

**#2 This wallet is written in c# with WinForms. Supports Win/Mac/Linux**

![]({{ site.baseurl }}/images/0AaIh-Tyrs97Ll9zt.png)

[turtlecoin/turtle-wallet-winformsturtle-wallet-winforms - Desktop GUI Wallet made w/ WinFormsgithub.com](https://github.com/turtlecoin/turtle-wallet-winforms)

**#3 This wallet is written in Python w/ Glade. Supports Win/Mac/Linux**

![]({{ site.baseurl }}/images/0DbzLQf8WzuLqePPs.png)

[turtlecoin/turtle-wallet-pythonContribute to turtle-wallet-python development by creating an account on GitHub.github.com](https://github.com/turtlecoin/turtle-wallet-python)

**#4 This wallet is written in Javascript w/ Electron. Supports Win/Mac/Linux**

![]({{ site.baseurl }}/images/0nzqf2OPbkqwETQgM)

[turtlecoin/turtle-wallet-electronturtle-wallet-electron - GUI interface based on Walletd for TurtleCoingithub.com](https://github.com/turtlecoin/turtle-wallet-electron)

**#5 This wallet is written in C#. Compatible with Windows, Testing Only**

![]({{ site.baseurl }}/images/0S0V24IVCNnA15_J7)

[turtlecoin/turtle-wallet-csharpturtle-wallet-csharp - An RPC based client wallet application built for use on the Turtlecoin (TRTL) network.github.com](https://github.com/turtlecoin/turtle-wallet-csharp)

- **The TurtleCoin Mining Pool Monitor —** app has been re-released on Android now, so that the iOS and Android features will be in-sync moving forward. It has also undergone a few updates recently: — now supports the unified pools list JSON — the pools screen now has last block found time and estimated average block found time — the dashboard now lists the last pool payment timestamp Download the app today! **— derp3xIOS —** <https://itunes.apple.com/us/app/turtlecoin-mining-pool-monitor/id1353746147?ls=1&mt=8>  
  **Android —** <https://play.google.com/store/apps/details?id=lol.turtlecoin.poolwatcher&hl=en>
- **TurtleNode.io —** daemons are updated to v0.4.3 and are running like champs. TurtleCoind-ha project received a major update this week that helps with stability quite a bit. Also added a few new features in support of v0.4.3 of TurtleCoin. See <https://github.com/turtlecoin/turtlecoind-ha/releases> for more information Most of my “spare” time this week was spent working on TurtleCoin itself. **— Iburnmycd**  
  [**https://turtlenode.io**](https://turtlenode.io/)
- **Wiki —** is getting a lot of revamp this week, big thanks to zed, guacamole and sajo and everyone for all the contributions and work keeping our documentation up to date, accurate, thorough and easy to follow **— bebop**  
  <https://github.com/turtlecoin/turtlecoin/wiki>  
  **_“_**_I’ve been making some big changes to the wiki. Changing the structure of files and adding newer guides on other topics. It’s been coming along nicely, excited to have it done and pushed to the wiki. It’s gonna be great :D”_ **_— Sajo_**  
  _“We have been updating the wiki to make it a one-stop-shop for all things TurtleCoin. I am hoping that if we can make the wiki as newbie friendly as possible, we can reduce the barriers of entry into our community. Come and give us a hand!”_ **— holyguacamole**
- **Simplewallet —** Hopefully those of you who are using simplewallet have enjoyed the UI changes that 0.4.2 brought. There’s a few new features in 0.4.3  
  The \`_— wallet-file\`_ and _\`— password\`_ args that some people were missing have been re-added, so you can start up your wallet straight away from a batch file or script. It also adds timestamps to list_transfers, so you can see how long you’ve been a part of this great community!  
  <https://github.com/turtlecoin/turtlecoin>
- **0.4.3 Fast Sync —** “The ability to sync the daemon using a list of checkpoints rather than maintaining bootstrap snapshots was added. This enables fast initial syncing and spreads bandwidth usage across the network rather than a single blockchain download and should aid in faster recovery of daemons when problems arise.”**— Ereptor**  
  <https://github.com/turtlecoin/turtlecoin>
- **New Algo —** “Turtlecoin has officially moved from Cryptonight to Cryptonight Lite Variant 1\. This was implemented via a collection of opportune if statements.” **— Suml Noether**
- **Nest GUI —** The Nest wallet is getting featured on turtlecoin.lol as the main GUI wallet. Coming from the industrial and startup spaces, where I developed many apps, but for internal use or for cocky bosses who thought they had the next big idea but nobody wanted their product, it’s a nice change. With already hundreds of users and soon thousands, it feels great to develop something people want and use, and to help grow the TurtleCoin community. **— Jon Nest Dev**

![Image result for turtle nest gui](https://miro.medium.com/proxy/0*IT8ecKV27Gw2t5rd.)

TRTL Nest GUI

- **TRTL Wear Watch App —** “trtl wear released this week, now you can see the time, date, weather and the vaule of a turtle coin all from your watch. Along with that I’ve been making some fresh exploration into getting android a turtle wallet, hopefully more on that soon.” **— Seperot**

![]({{ site.baseurl }}/images/0rP-R7TXK2vAALMoU.png)

turtle-wear

- **Winforms GUI —** We’re actively working on the WinForms wallet, making continuous progress by resolving github issues, adding features, and keeping an eye on #help and #wallets for any issues that haven’t been reported yet. **— JerMe404**

![]({{ site.baseurl }}/images/1p9mKVtsFzZSmAXtPvwmq7g.gif)

Winforms GUI

- **Electron GUI —** The newly introduced Electron GUI wallet, named WalletShell, has just entered the GUI wallet race. It’s main goal is to provide users with an intuitive and pretty looking interface. Future updates will include a revamped Transactions page and the ability to use a public node. **— PermaDeath**

![]({{ site.baseurl }}/images/1Y370dLXUghBpHLygCBgahA.png)

Electron Wallet

- **Turtle Racing Alpha —** tests have been running through the week and collecting/fixing bugs. Check out videos and follow on Twitch <https://www.twitch.tv/turtleracingalpha/videos/all> The next features being worked on is a turtle auction where you can buy and name your own turtle with max speed, acceleration, and endurance stats that effect the outcome of the races, and exacta and trifecta betting pools. **— Ryan**

![]({{ site.baseurl }}/images/10vrTsgl4u47aU_kT-5g1Ow.gif)

Turtle Racing

- **RocksDB Upgrade —** As Turtlecoin community was screaming to heavens “Oh Great Turtle, please pretty please, bless us with stable daemon!” two brave turtles with capabilities heard the prayers. Here we are now blessed with daemon stable more than EVUR! **— YamiM0nster**
