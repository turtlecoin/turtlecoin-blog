---
layout: "post"
title: "This Week In TurtleCoin (July 23, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0RAWpSgHmW8rAL59Q.gif"
date: "2019-07-24T04:49:42.491Z"
---

![]({{ site.baseurl }}/images/0RAWpSgHmW8rAL59Q.gif)

This guy’s hairline is better than mine and that is perfectly okay.

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post, click [this link](https://goo.gl/forms/BNaRYkUmOVOa1apQ2)

![]({{ site.baseurl }}/images/0W1EyqJLekzwZl0\_-)

**TurtleAds**

TurtleAds is an ad platform for TurtleCoin. You can advertise your node, website or anything else and pay with TRTL. Then people who own websites can embed your ads and will get paid for it. The project is still in a very early development phase and will launch in the next 2 to 3 months..

**fipsi#0789**

![]({{ site.baseurl }}/images/09J8T4Ayc4aNe*zy*)

Sabo, Revolutionary (Pictured) surrounded by public node earnings

**Public Node**

I have just set up a node for a project I am working on, meanwhile feel free to connect to this public node.

**Sabo (Revolutionary)**

[http://165.22.97.214:11898](http://165.22.97.214:11898/)

![]({{ site.baseurl }}/images/0nAj-NtnIPCjSpS1z.jpg)

Hey kid, you ever had a TPN? \*opens coat\*

**TurtleCoin public node setup guide**

For when you want to run an awesome public node but are on a very tight budget.

This guide covers the entire setup and build of the TurtleCoin public node as well as running it. It also covers the setting up of the front page for the public node. This guide was tested with various versions of Ubuntu using Google Cloud virtual machines with the aim of ultimate cost effectiveness and ease of use..

**forcejunky**

[forcejunky/turtlecoin-budget-public-node-guideTurtleCoin public node setup guide. For when you want to run an awesome public node but are on a very tight budget. …github.com](https://github.com/forcejunky/turtlecoin-budget-public-node-guide)

![]({{ site.baseurl }}/images/0Yz3zC6Yq13e3IhNQ.gif)

Crypto lib’s just purrin’ like a cat

**TurtleCoin-Crypto**

I’ve performed a few small updates to the TurtleCoin-Crypto project that helps to make life a bit easier.

1. Javascript builds (.js and WASM) now build to single files to make it easier to import for packing.

2. Enabled a handful of optimizations that reduce the Javascript & WASM build file sizes significantly and results in slightly faster code execution.

3. Added Node v12 support

4. Added support for gcc 4.x versions for those of us running ancient build systems (dropped requirement to c++11)

**IBMCD**

[turtlecoin/turtlecoin-cryptoTurtleCoin: Standalone Cryptography Library. Contribute to turtlecoin/turtlecoin-crypto development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-crypto)

![]({{ site.baseurl }}/images/0l9agk7RhFKr1Tssw.png)

**TurtleCoin-Utils**

A bit of work was done on this package to make it easier to work with TurtleCoin data:

1. Added support for Node v12 (thanks to TurtleCoin-Crypto updates)

2. General code cleanup

3. Added exports for the underlying Crypto module (in the event you want to get your hands dirty)

4. Added export for new Block object that allows for deserializing and serializing blocks to/from blobs. It also allows for the calculation of the block id (hash) as well as the PoW hash.

5. Added export for new Transaction object that allows for deserializing and serializing transactions to/from blobs. Also provides a property for the transaction prefix hash as well as the full transaction hash (when loaded with signatures) and supports version 2 transactions.

Next up, I’ll be working on the necessary transformations for handling block templates for mining pools.

**IBMCD**

[turtlecoin/turtlecoin-utilsNode.js utilities for working with the TurtleCoin network - turtlecoin/turtlecoin-utilsgithub.com](https://github.com/turtlecoin/turtlecoin-utils)

![]({{ site.baseurl }}/images/0okoD_oRwIaLMb4oK.gif)

If you write about your backend and don’t include a pic, this is what happens.

**turtlecoin-wallet-backend**

Lots more updates to the JS wallet backend this week. These have mainly been fueled by extra’s new GUI wallet, proton, finding bugs and requesting features — check if out if you haven’t already.

_Updates include…_

- Faster syncing in some environments
- Fix bug when sending transactions to self
- Fix bug with locked balance not been correctly updated
- rewind() function, and daemon connection status events
- Faster cryptography for those in a browser env thanks to turtlecoin-utils upgrade

If you didn’t know already, this library lets you create, import, sync and send transactions all from JavaScript. A lot of people have started building applications on top of it, and I’m excited to see what more can be built.

Check it out: <https://github.com/turtlecoin/turtlecoin-wallet-backend-js>

**Zpalm**

![]({{ site.baseurl }}/images/0WpUAcUbWAcMCUSyn)

**TonChan**

A few weeks ago I promised an update to TonChan, unfortunately, that slipped a little. I got distracted upgrading React Native for 64 bit builds which caused me to spend a lot of time fixing the build for the newer library.

That is all done now, and I’ve decided to add a few more features than planned to the release.

_Currently implemented:_

- 64 bit support
- Faster syncing
- Auto optimize support
- Better memory management
- Icons that fit better with Android style
- Faster transaction creation
- Tons of bug fixes

And before a release, I also want to improve the background syncing process, and possibly add transaction filtering and fingerprint unlocking.

Hopefully these won’t take so long to implement.

**Zpalm**

![]({{ site.baseurl }}/images/0p5byDbxgOBf41Gga.jpg)

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

**Daemon+WalletBackend timestamp adjustments**  
The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away).  
<https://github.com/turtlecoin/turtlecoin/issues/704>

**Remove no longer relevant asserts**  
Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.  
<https://github.com/turtlecoin/turtlecoin/issues/811>

**QueryBlocksDetailed does not populate transaction extra “raw” property in response**  
`.transactions[i].extra.raw` is not populated in the code as it should be.  
<https://github.com/turtlecoin/turtlecoin/issues/815>

![]({{ site.baseurl }}/images/0C6wGIqJTxt3BVXCs.jpg)

## Pay With TRTL

In the Discord we have a channel called #Merchandise where people can post things you can buy with TRTL. To view items for sale, check the pinned posts in that channel. These are a few of the items from this week.

**mikeykones’s dad hats**

TURTLECOIN DAD HATS 🧢 199k TRTL free shipping anywhere in the US, 299k TRTL shipped anywhere else in the world!

Red, black, grey and cream are available currently

**Contact @MikeyKones in discord for details!**

![]({{ site.baseurl }}/images/0c-v6gpP5Or74yDJO.gif)

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- Hi :) I’m working on a new game for Turtlecoin. It’s a web based card game where you can collect the emojis from the discord and then fight other players using them. The game will launch in the next 10 days, if you want to stay informed about updates join my discord server. Hope to see you there :) <https://discord.gg/USK4Zvb>
- I updated my node to 14.6! [http://turtle.japakar.com](http://turtle.japakar.com/)

![]({{ site.baseurl }}/images/01En39VilZUmrCuKJ.png)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- SoreGums — “stay gone” your game is cool, <https://shellwars.de.cool/> — I like the graphics and UI, looking forward to see what you do next :)
- JAPAKAR.com — Thanks again to the community! As always! You guys rock :)
- Japakar King of the Ozarks — Youre all welcome into my Ozark forest. There is magical fairies to eat, they taste like frogs.
- Ｄｕｎｇｅｏｎ Ｍａｓｔｅｒ — Thanks to all who were part of the adventure this week, let’s shoot for sometime between Friday and Sunday
- Rock — Shouts out to all the comedians with heart out there crackin jokes to two man crowds

![Image result for site:imgur.com ballin](https://miro.medium.com/max/60/0*mpjILA7shPHWpyg9.jpg?q=20)

![Image result for site:imgur.com ballin](https://miro.medium.com/max/1400/0*mpjILA7shPHWpyg9.jpg)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-23-2019/)_._
