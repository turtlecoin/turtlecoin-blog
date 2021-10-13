---
layout: "post"
title: "This Week In TurtleCoin (Jan 21, 2019)"
description: "cryptonote-nodejs-pool — I’ve just finished updating the pool software for the upcoming fork, building on the fine work of the Plenteum developers. Check it out in action at fork-o-clock, over at…"
image: "{{ site.baseurl }}/images/01i9m5QADy-W07tls.gif"
date: "2019-01-22T05:56:33.637Z"
---

![]({{ site.baseurl }}/images/01i9m5QADy-W07tls.gif)

# Developer Updates

![]({{ site.baseurl }}/images/0SiQOzqScJD4tavKw.jpg)

**cryptonote-nodejs-pool —** I’ve just finished updating the pool software for the upcoming fork, building on the fine work of the Plenteum developers. Check it out in action at fork-o-clock, over at [https://trtl.heigh-ho.funkypenguin.co.nz](https://trtl.heigh-ho.funkypenguin.co.nz/) :) **— funkypenguin**

[funkypenguin/cryptonote-nodejs-poolMining pool for all CryptoNote based coins using Cryptonight, Cryptonight Light and Cryptonight Heavy algorithms …github.com](https://github.com/funkypenguin/cryptonote-nodejs-pool)

![]({{ site.baseurl }}/images/045Yf2aViQFml2a7L.png)

**Mobile Wallet —** Hello, Not sure when I last gave an update. I have done most of the work on the wallet backend, and now I am starting on the mobile app UI. It’s a lot easier to find bugs when you start actually making the wallet. This probably will be the easiest part of making the wallet, but I’m not great at design so it’s a little slow. I’m not sure how tricky it is to get iOS wallet apps onto the App Store these days — I was under the impression they didn’t allow them, but I did recently see another relatively small crypto who had got a wallet on there. Fortunately react native supports iOS, so once the Android is done, I will certainly look into it. Not a massive fan of the license fee you have to pay, nor do I have an iOS device for testing… but at least we won’t have to write much more code. Thanks to iburnmycd for his turtlecoin-utils module — This has taken a decent amount of the hard bits of code to write off my shoulders. I recently also added support for syncing via the TurtlePay blockchain cache API in the backend — (<https://docs.turtlepay.io/blockapi/>) — currently this isn’t much faster than a daemon, however, I think it will probably have much better uptime, which should help avoid people wondering why their wallets are not syncing. **— Zpalm**

[zpalmtree/ton-chanA mobile TurtleCoin wallet. Contribute to zpalmtree/ton-chan development by creating an account on GitHub.github.com](https://github.com/zpalmtree/ton-chan)

![]({{ site.baseurl }}/images/0zI4fer00KxnrvD9V.png)

**TRTLfarm** — TRTLfarm is an online virtual farming game build on top of TRTL.services by Boris. People can buy farm animals with TurtleCoin, which return produce based on their programmed production speed. The game started out as a small project, but has blown up quickly. Boris has working hard past few days and just finished implementing a leaderboard where turtles can track their rank. While I will giving the UI a touchup, Boris will be working on a surprise! Join us in the discord to discuss development and provide feedback! <https://discord.gg/X7b7GWW> **— fexra**

[Production area - TRTLFarmTRTLFarm is a farming simulator and idle game played with and for TurtleCoin using TRTL-Services. The more animals you…trtlfarm.com](https://trtlfarm.com/)

![]({{ site.baseurl }}/images/0IErcYtovppbzgDmC.png)

**WalletShell —** Got help from very nice friends, who was willing to help me debugging and provides a tested macOS build. New macOS build is available here: <https://github.com/turtlecoin/turtle-wallet-electron/releases/download/v0.3.7/WalletShell-v0.3.7-mac.dmg> It’s confirmed to be working, but was only lightly tested and there may be bugs slips here & there. So if you happened to found one, please file a bug report on github. Thanks to @greywolf & @Messier_45 for your help! **— labaylabay**

[turtlecoin/turtle-wallet-electronGUI interface based on Walletd for TurtleCoin. Contribute to turtlecoin/turtle-wallet-electron development by creating…github.com](https://github.com/turtlecoin/turtle-wallet-electron)

**CryptoNode Helper —** Since I learned to use Docker for serving my TurtleCoin public node, I decided to script some of the commands I was using a lot. I chose to do it in a way that other people may benefit; and also to improve my coding skills along the way. Six weeks later; I have something that works well enough to share. In the video, I spin up a daemon in less than 5 minutes (excluding compile time and syncing the chain), and start the CPU miner. The repo comes with a few examples you can use yourself or adapt for your own CN coin. Feel free to raise issues on the GitHub or contribute some code yourself. It’s not perfect by any means, but it’s what I use! **— Morpheus**

[Using Cryptonote HelperWelcome! In this recording, we install and run the 'CryptoNote helper script' to install and run a CN fork. For this…asciinema.org](https://asciinema.org/a/222640)

[19morpheus80/helperHelper script for downloading and running CryptoNote currency in Docker - 19morpheus80/helpergithub.com](https://github.com/19morpheus80/helper)

**TurtlePay —** It’s been a busy week but I managed to get the callbacks documented at [https://docs.turtlepay.io.](https://docs.turtlepay.io./) This week I’m hoping to find time to build out a few more API calls for advanced developers. **— IBurnMyCd**

[TurtlePayTurtleCoin payments processing for developers, by developers.turtlepay.io](https://turtlepay.io/)

**Nest Multiple Language Support** — I added internationalization support to the Nest wallet! Nest now detects your OS locale, and displays in your language if a translation file has been added. **— Turtley McTurtleton**

[jerme404/turtle-nest-forkTurtleCoin Nest wallet, easier to fork than ever! Contribute to jerme404/turtle-nest-fork development by creating an…github.com](https://github.com/jerme404/turtle-nest-fork/blob/i18n/docs/translating-nest.md)

**Raspberry PI Daemon Guide** — I wrote a little guide to get set up with pi64 and running a node on a raspberry pi 3 b to celebrate ARM builds being fixed! Check it out and feel free to suggest improvements. Thanks **— ExtraHash**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/wiki/Running-TurtleCoind-on-Pi)

**TurtleCoind finally runs like a charm on ARM(Pi) —** The long wait is over. You can now run your TurtleCoin node on ARM(Pi). Over the past 1 month and many sleepless nights, we’ve finally cracked the segmentation fault problem with the TurtleCoin daemon on the ARM64 architecture. Now your node will run happily on any of your favorite 64-bit SoC board, such as Raspberry Pi 3(+), OrangePI One Plus, Rock64(Pine) and many more. If you are an early adopter and would like to test it, all you need is to clone the development branch of the TurtleCoin repo from github and compile your own binaries. We will release and publish the binaries for you to download for the ARM platform with the next scheduled release. Thank you to @iburnmycd, @thinkpol, @zpalmtree, @rashedmyt, @fexra, as well as to my dear wife @imrealeqra for waking me up from taking a nap on my keyboard every day in the past month around 5am morning :) **— LeoCuvée #1481**

# From The Blog..

- Fexra interviewed Boris, the creator of TRTLfarm, a game built on top of TRTL Services — <https://blog.turtlecoin.lol/archives/virtual-farming-with-boris-from-trtlfarm/>
- Rock interviewed FunkyPenguin, a hard working member of the TurtleCoin community who has taken mining pool setup to new levels using Docker — <https://blog.turtlecoin.lol/archives/funkypenguins-turtle-pool-secrets/>
- SoreGums, The Lost Interview — <https://blog.turtlecoin.lol/archives/interview-w-soregums-from-trtl-core-team/>

# Promote Your Bounty!

**50,000 TRTL** — it is good for the marketing, i think it is perfect **— Guang**

**140,000 TRTL —** Make an open-source, easily integratable web miner for turtlecoin and optionally host it on your own website. **— Sajo8**

# Community Advertising

- Two brand new community projects to check out already this year! Who sent 10 turtle by MrRovot and a custom minecraft server by WarLordN1k. So come any play all the communities amazing games @ [games.turtacus.com](https://games.turtacus.com/)
- FREE public node, one of the only free ones left. greywolf Germany turtlenode.co <http://turtlenode.co:11898/feeinfo>
- TurtleDice — Bet and try your luck with this new gambling website. You choose your winning chances and we roll the dice for you! No registration, fair and fun playing! [https://turtledice.de.cool](https://turtledice.de.cool/)
- Free Turtle Coin for cool dudes! Yup thats what we have here. Just click the link, collect your coin, and be excellent to each other! [https://trtl.faucet.llama.horse](https://trtl.faucet.llama.horse/)
- FREE public node — one of only 3 FREE public nodes remaining. you can connect the CLI or Nest wallets to this FREE public node, based on 4 core Xeon, 200GB SSD, 8GB RAM VPS, located in Germany. <http://turtlenode.co/connect/connect-to-node.html>

# Shoutouts & Thanks

Rogerrobers — Shout out to CapEtn

Captain Jac) — Shoutout to all turtles and welcome to all new ones

DazCat — I want to thank everyone in Discord for the warm welcome and quick answers to my questions :)

rock — I may have forgot to erase some of these from last week..

rock — shouts out to the people who leave funny pics and msgs in the roundup form with no descriptions. It always gives me a chuckle :)

BobbyBlank — Props to everyone who make TurtleCoin possible — from the humble gang of developers, to the community-at-large. Thanks for doing what you do, everyone — keep up the great work!!!

Sups — Great collaboration, Plasticus and Bazza working together to get the block Explorer working properly, nice work guys!

Specter — No matter how bad things seem to be, be thankful you are alive, that can all end in an instant, so fast, and nothing we can do to stop it. Take a moment to tell a loved one or a friend how much they mean to you. Don’t live with that regret.

LabayLabay — @greywolf for being super nice, wish you all the best!

canti — I met a homeless man on my way home from work today. He was convinced he was Steve Jobs and that the CIA faked his death to benefit capitalism, despite looking like Gary Oldman’s 20 year older brother. I had a morbid curiosity that made me want to hear out his ramblings, so I sat down to listen to his story. He told me he was in his prime and on top of the world until he brought up an idea he had to the overlords at Apple. (“Overlords” was his word not mine, just thought I’d throw that in.) This idea, it turns out, had to do with Apple’s stance on privacy, business, and innovation, and how he wanted to expand it into the monetary world. He told me how this idea, particularly how he wanted to bring it about, didn’t particularly jive with the other higher ups, whom he called “The Suits”; they only saw dollar signs in their eyes. Fast forward a few years now — after replacing him with a frail lookalike for public appearances, they ultimately faked his death, and go on to release Apply Pay back in 2014, which he says was a bastardization of what he wanted to bring to the world. But what about our protagonist? Well, he said by this point he had already been ostracized from the company and rejected by his peers, so he had delved back into the shadows, working in privacy on his true vision. He said he worked on a project with a couple friends for a while that went the wayside, but ultimately led him to where he’s at now, slowly working to make his dream a reality. The man I met? He wasn’t homeless at all as I originally thought, just a bit disheveled and maybe a bit stoned. Today I met RockSteady, the founder of TurtleCoin, and found out the secret behind his true identity.

japakar — <http://prntscr.com/m9zfwf>

Rock — Shoutout to Teacup for all the art! Thanks to all the release testers! Big thanks to WZA for the neighborliness! shouts to Alien for the diversified input sizes! big whats up to the turtles we only see during _certain times of year.._ shout out to that scrawny kid Connie I ran in to on mushrooms at the vegan market!

See you guys next week :) Go teach a friend something!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-jan-21-2019/)_._
