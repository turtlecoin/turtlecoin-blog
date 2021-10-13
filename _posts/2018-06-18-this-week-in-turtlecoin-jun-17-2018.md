---
layout: "post"
title: "This Week In TurtleCoin (Jun 17, 2018)"
description: "This week we added a new core contributor, deployed a new and improved block explorer, announced a new CLI wallet, made yet another web…"
image: "{{ site.baseurl }}/images/1GEmQlJh2FqOMjHiF9VjsMQ.png"
date: "2018-06-18T17:47:25.775Z"
---

## This week we added a new core contributor, deployed a new and improved block explorer, announced a new CLI wallet, made yet another web wallet, ripped out some code and stuff we probably shouldn’t be touching, and **more…**

![](https://miro.medium.com/max/3812/1*GEmQlJh2FqOMjHiF9VjsMQ.png)Zedwallet is a CLI wallet written 100% from scratch that can be used by any Cryptonote coin with very few modifications. Collaborators wanted!

# And now for this week’s updates…

Zedwallet \[Pictured Above\] —Zedwallet is a new CLI wallet that replaces Simplewallet in TurtleCoin, and really any Cryptonote coin with very few modifications. In this wallet we have in-wallet fusions, transaction splitting, and an improved user experience. We recently did an in-depth article detailing the work that went into the new wallet with the creator himself.

[Zedwallet, A New Simplewallet for CryptoNote CurrenciesSome of you may have noticed in the last few releases that Simplewallet has been looking a bit more polished. In fact…medium.com](https://medium.com/@turtlecoin/zedwallet-a-new-simplewallet-for-cryptonote-currencies-2c74c5fc1302)

![]({{ site.baseurl }}/images/1pycmet7Jw-igj13IGXMiLQ.png)

TurtleNode.IO Block Explorer — htps://blocks.tutlenode.io

**TurtleNode.IO Remote Daemon & Explorer —“**_I’ve spent this week working on speeding the TurtleNode.io block explorer. Considerable effort has been put forth to create a lightning fast block explorer with full historical capabilities that is driven by fast cache mechanisms and other performance enhancements. Additional enhancements are being worked on that will make the service even faster. Check it out at_ [_https://blocks.turtlenode.io_](https://blocks.turtlenode.io/)_. In other news, I’ve rebuilt all of the load balances for the public nodes and as a result, direct access to each of the nodes is no longer supported. Please make sure that you’re using one of the region based hostnames as listed on_ [_https://turtlenode.io_](https://turtlenode.io/) _or simply public.turtlenode.io_” **— iburnmycd**

[**https://blocks.turtlenode.io**](https://blocks.turtlenode.io/)

![]({{ site.baseurl }}/images/0x37sK68NTMEovNCd.png)

This is modern art, courtesy of a time warp attack on the network.

**Difficulty Algorithm —**_“After about a month of testing, and tweaking, the LWMA-2 difficulty algorithm is ready to go! It’s been merged into the main codebase, and will go live at an appropriate block height once the next release is made. This should reduce the profitability of pulse mining, prevent timewarp attacks from freezing the network, and make the difficulty just a lot more reactive. Thanks to zawy for his work on this and SoreGums for running all the testnet infrastructure!”_ **— ZpalmTree**

[Hard fork at 600k to use LWMA-2 difficulty algorithm by ZedPea · Pull Request #293 ·…After weeks of testing and tweaking zawy has arrived on the perfect difficulty algorithm... for now! This also applies…github.com](https://github.com/turtlecoin/turtlecoin/pull/293/files)

![]({{ site.baseurl }}/images/0C-JXP6SzkzfmOXfX.png)

a rare peak at Fexra’s TurtleWallet Web Wallet backend, rumored to be engineered by magical elves formerly employed by Elon’s personal moles at CERN.

**Fexra’s TurtleWallet Web Wallet —**_“ After more than two weeks of sweat and tears and lots of help from all the good turtle devs, I finally finished converting all the workers that read incoming and outgoing transactions to a much more efficient and stable system. I want to thank all of you for being so patient and giving it another try! If you haven’t yet, come and join us at_ [_https://chat.turtlewallet.io_](https://chat.turtlewallet.io/)_”_ **— Fexra**

[Welcome | TurtleWalletFexra’s TurtleWalletbeta.turtlewallet.io](https://beta.turtlewallet.io/)

![]({{ site.baseurl }}/images/0t4QfcR8T72A6Ckel.png)

**TRTL featured in “Token Party the Cryptocurrency Game”! —** _I finally published my cryptocurrency-board game! “Token Party” includes two special “TurtleCoin Mining” cards, the only real coin in the hardware deck. Thank you RockSteady for your blessing :)_ **— Andready**

[Token Party: the cryptocurrency gameToken Party is a cryptocurrency-world based game for 2-6 players. The goal of the game is to stash a big amount of…www.tokenpartythegame.com](http://www.tokenpartythegame.com/)

![]({{ site.baseurl }}/images/0TGMjvXoBdrpLYIG5.png)

Box-Turtle, A host your own at home web wallet for people who don’t trust or need an online hosted web wallet.

**Box-Turtle Host Your Own Web Wallet —**”_The goal here was to get a little web wallet you can run locally on a Raspberry Pi at home. We ran into some snags with getting our code compiling on a Raspberry Pi, and in fact there’s a bounty of over 1MM TRTL to get the code compiling on a Pi, just because we think it’s that cool of a project. In the mean time, however, we are working to turn it into a self contained VirtualBox appliance you can host at home. Eventually, we want to be able to make a bunch of these Turtle-Pi’s and bring them to weekend hackathons in youth communities to get new users acquainted with TRTL and some light blockchain related development with a low target cost and high potential for usability. Community buy in is important to fulfill our mission to educate those that aren’t already crypto-savvy.”_ **_— RockSteady_**

[turtlecoin/box-turtlebox-turtle - Host Your Own Web Wallet In A Boxgithub.com](https://github.com/turtlecoin/box-turtle)

![]({{ site.baseurl }}/images/0gHkZho7mFgN_yMBN.png)

![]({{ site.baseurl }}/images/0orEH8Z-VDttt8CbN.png)

[**TurtleCoin.supply —** TurtleCoin current and future supply on a beautifully designed graph by Mrrovot](http://turtlecoin.supply/)

**Mrrovot’s TurtleCoin.supply** — “_network supply visualization on an interactive graph, just stunning to look at and interact with using the mouse._”

![]({{ site.baseurl }}/images/0gfyqAxfVvOakUQI0.jpg)

These are the actual game graphics if you imagine them hard enough. Think about it. Look into it.

**Gladiator Bot —** _“Gladiator introduced weekly tournaments last Sunday with the top Gladiator being awarded 10,000TRTL at the following Sunday. This week, potions have been introduced! You can now purchase potions from Gbot at 150 TRTL each for recovering 20hp for use in battles. This should help keep Gladiator Bot funded and able to continue offering the prizes he offers! Next stage is stats!”_ **_—_ Rynem**

[Rynemgar/Gladiator-BotContribute to Gladiator-Bot development by creating an account on GitHub.github.com](https://github.com/rynemgar/gladiator-bot)

![]({{ site.baseurl }}/images/0Ti9IxHveKo036obH)

**Funky Penguin’s NZ Turtle Stew^H^H^H^H Pool —“**_Nothing much to report, been tied down with other projects and responsibilities. However, NO daemon/sync issues in the past few weeks. Working with turtleminers.club on testing some improvements to the dockerized mining pool design this week._” **— Funky Penguin**

[Funky Penguin's NZ TRTL Mining PoolEdit descriptiontrtl.heigh-ho.funkypenguin.co.nz](https://trtl.heigh-ho.funkypenguin.co.nz/)

# Shoutouts

**zpalm —** Shoutout to Soregums for keeping tons of test infrastructure running for me and canti! \\o/

**Rogerrobers —** Shout out to Morocco for scoring an own goal in the 95th minute

**zpalm —** I love the shoutouts!! Keep doing them, even if they’re dumb! PS hai pls come play bitcorn

**Khorosho —** Shout out to the devs and users that work their asses off to make a good coin with a great user base-you’re the best in having a good user user base with out hate or market talk all day!

**RockSteady —** Shouts out to Funky Penguin for making the coolest tutorials in the land.. to rynem for an ever evolving battle I never can seem to win.. to mrrovot for making numbers even more beautiful.. to Canti for keeping his legs.. to Andready for always thinking of the home-team :).. for Fexra, ZPalm, Soregums, Iburnmycd and the rest of the Turtles for putting up with my crickets and my bullshit questions.

**Rocksteady —** Shouts out to you, reader, I’m happy to share this community experience with you :)

## P.S. Happy Birthday to Tipp and Alien and get well soon, Canti

![]({{ site.baseurl }}/images/0P8WvuAg9VgXHowhR)

oh and word on the street is we’re being added to a new exchange that is just starting out. enjoy :) — rock
