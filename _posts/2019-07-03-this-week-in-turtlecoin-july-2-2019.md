---
layout: "post"
title: "This Week In TurtleCoin (July 2, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0wDID4iDPTDDYOk31.gif"
date: "2019-07-03T01:33:57.171Z"
---

![]({{ site.baseurl }}/images/0wDID4iDPTDDYOk31.gif)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post,_ [_click this link_](https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform)

![]({{ site.baseurl }}/images/0avWDpHhgCIrXL9KJ)

Chukwa’s Labyrinth

**Chukwa’s Labyrinth**

I started making a new TurtleCoin-themed game, “Chukwa’s Labyrinth”! You’ll have to go through a series of mazes in order to reach the prize at the end! So far I’ve gotten player movement, a turtlecoin powerup and basic levels designed. I’m currently working on refining my tilesets and how I approach tilemaps. I’m using Godot Engine — a free, cross-platform, open source engine. It’s extremely powerful, 2D and 3D, and is licensed under the MIT license(!). No royalties, no strings attached.

My game will be released under the GPLv3 license, you can check out the code at the GitHub repo. Big shoutout to @oiboo for making all my art for me, you rock. Also kenney.nl for his amazing artpacks! And also thanks to @GT3000, for helping me get started and giving a great starter resource

**Sajo8**

<https://github.com/Sajo8/chukwas-labyrinth> <https://godotengine.org/> <https://gist.github.com/GT3000/eee456bdfa3ba8c31fa1dafd085e2b2e>

Proton Wallet — A TurtleCoin Wallet

**Proton Wallet — A TurtleCoin Wallet**

Hey everybody, as some of you may have heard, I’m developing a GUI wallet using the new and very capable wallet backend. The new backend was written by everyone’s favorite developer, the handsome @zpalmtree. It’s a really huge improvement over the old turtle-service based wallet applications as the wallet interaction is all done in pure javascript with no need for laggy RPC connections or mucking about running other processes, which leads to less lagginess and overall a better user experience.  
Down the road I’m planning on implementing some more advanced multi-address wallet features, and I’d also like to see it become a full-fledged multi currency wallet. I think many users are tired of having so many different wallets installed on their computer: a really nice multi-currency wallet could really attract a lot of users.  
Please test out the beta version which should be released in a few hours at <https://github.com/turtlecoin/turtle-wallet-proton/releases> and get back to me with your feedback.

**ExtraHash**

[turtlecoin/turtle-wallet-protonContribute to turtlecoin/turtle-wallet-proton development by creating an account on GitHub.github.com](https://github.com/turtlecoin/turtle-wallet-proton/releases)

![]({{ site.baseurl }}/images/0kB5mmoat4NNIFi_h.png)

**TurtleCoin Added to Shrimpy App**

**TurtleCoin Added to Shrimpy App**

I wanted to pass something along for the weekly update. TurtleCoin has been added as a supported coin on Shrimpy this week. It is a cryptocurrency rebalancing app. It will automatically rebalance your portfolio based on your long term strategy.

**uaoverall**

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

- **Add type assertions for JS users**  
  Currently you can pass incorrect types to functions without it throwing. This usually causes hard to diagnose errors. We should add assertions to check each type is as expected, and throw if not.  
  <https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/16>
- **Add swap node method**  
  Take an `IDaemon`, update the stored daemon (this is passed down to a few sub-classes, so might want to use the `initAfterLoad` method?), init this stored daemon, and start it fetching data.  
  <https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/22>
- **Improve auto optimization**  
  Right now we only auto optimize on receiving a transaction, when the wallet is close to synced. If a user rarely opens up their wallet, then the wallet may never be synced when receiving a transaction.  
  <https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/24>
- **Daemon+WalletBackend timestamp adjustments**  
  The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away).  
  <https://github.com/turtlecoin/turtlecoin/issues/704>
- **Remove no longer relevant asserts**  
  Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.  
  <https://github.com/turtlecoin/turtlecoin/issues/811>
- **QueryBlocksDetailed does not populate transaction extra “raw” property in response**  
  `.transactions[i].extra.raw` is not populated in the code as it should be.  
  <https://github.com/turtlecoin/turtlecoin/issues/815>

## Bounties

_Bounties are a great way to earn TRTL for doing small tasks, and also a good way of getting things done if you want something made and have some TRTL to spend._

- **20,000 TRTL** Get TonChan (<https://play.google.com/store/apps/details?id=com.tonchan>) added to the TurtleCoin website, by making a PR to <https://github.com/turtlecoin/turtlecoin.lol/> and having it merged. It should fit in with the rest of the website, so there should be an ‘Android’ entry added to the existing Apple, Windows, and Linux options.
- **\_100k TRTL_Merchandise** bot that will keep price for listed items in #merchandise updated in $TRTL according to actual fiat exchange rate without mentioning the fiat in the listing. @Elkim | trtl.urmom.lol 100k TRTL

## Pay With TRTL

_In the_ [_Discord we have a channel called #Merchandise_](https://discord.gg/jc5Traq) _where people can post things you can buy with TRTL. To view items for sale, check the pinned posts in that channel. These are a few of the items from this week._

![]({{ site.baseurl }}/images/08YxVhyQI5lAYBh_9.gif)

**TURTLECOIN DAD HATS 🧢**

**TURTLECOIN DAD HATS 🧢**

199k TRTL free shipping anywhere in the US, 299k TRTL shipped anywhere else in the world.  
Red, black, grey and cream are available currently

**mikeykones**

## Shoutouts & Thanks

_This is the place to mention someone in the community who has done something nice or deserves recognition._

![]({{ site.baseurl }}/images/0ZGG0bQlbwCyc-3HY)

Safari, y u do us like this

Shouts out this week to TurtleMax for pointing out a crazy CSS error on the main site when you view it in Safari. This one’s actually an old bug that we thought had been fixed, but it looks like safari didn’t get fixed at the same time. Good eye! — Rock

Big thanks to the lads who were able to make it last week for DnD, it was really fun and I can’t wait to see what happens this week — Rock

Also Thanks to xiaomogwai for this TRTL wallpaper :D

![]({{ site.baseurl }}/images/0fGl_1v_pPazH3L_Y)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-2-2019/)_._
