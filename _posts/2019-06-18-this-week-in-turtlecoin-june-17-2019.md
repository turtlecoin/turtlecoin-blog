---
layout: "post"
title: "This Week In TurtleCoin (June 17, 2019)"
description: "In this issue we all post shocked pikachu emojis when people forget to upgrade their miners for Chukwa and we mine all the TRTLs without them ;) For more info about Chukwa…"
image: "{{ site.baseurl }}/images/0YN_-HLTKJxRat9T-.png"
date: "2019-06-18T01:43:49.927Z"
---

![]({{ site.baseurl }}/images/0YN\_-HLTKJxRat9T-.png)

![]({{ site.baseurl }}/images/03L8iZCB-1B8u4p-e.png)

From the Teacup Files <https://blog.turtlecoin.lol/archives/the-teacup-files/>

## Developer Updates

![]({{ site.baseurl }}/images/03cot-r-Vz29nV51D.gif)

_In this issue we all post shocked pikachu emojis when people forget to upgrade their miners for Chukwa and we mine all the TRTLs without them ;)_

**For more info about Chukwa:** <https://blog.turtlecoin.lol/archives/the-quest-for-decentralized-proof-of-work/>

**To update your core:** latest.turtlecoin.lol

**The countdown until upgrade:** <https://explorer.turtlecoin.lol/>

![]({{ site.baseurl }}/images/03VfYEExRxV63JhIA.png)

**The Teacup Files**

Teacup has returned with a bountiful harvest of memes! Check them out here <https://blog.turtlecoin.lol/archives/the-teacup-files/>

![]({{ site.baseurl }}/images/0u68ftPJ33TXPAMXC.png)

**Rotate Discord Server Invite Backgrounds**

Discord’s new Nitro Boost stuff allows for Discord owners to choose custom background images when people use the invite links. However it means people have to manually click buttons in the Discord app.

So please head over to <https://support.discordapp.com/hc/en-us/community/posts/360047859252-Add-API-endpoint-for-server-invite-background> and upvote this post to encourage the Discord developers to expose this feature in the Official API. **SoreGums**

[Add API endpoint for server invite backgroundWe want to rotate the image using community created art. Since we're not supposed to use the endpoints discord use…support.discordapp.com](https://support.discordapp.com/hc/en-us/community/posts/360047859252-Add-API-endpoint-for-server-invite-background)

![]({{ site.baseurl }}/images/0Iq42nqX1Nk1-f0qF.gif)

**TurtleCoin Github Bot**

I’ve been looking into supporting multiple people making an issue at once with the Github bot; it doesn’t seem like it’ll be too hard to add, and it’ll be a nice little perk. If you don’t know what the Github bot is, I recommend you check it out! It lets you easily create a Github issue on any turtlecoin repo w/out an acc; type `!tag issue` in the `#bots` channel to learn more

**Sajo8**

![]({{ site.baseurl }}/images/0gWls0BhVOilFccJV.gif)

**turtlecoin-crypto**

As mentioned last week, I’ve been working on combining the different versions of this repo together. Good news! It’s done.

This repo now builds the following:

1. A c++ static library (Windows, Linux, OSX)
2. A shared library via DLL (Windows) that can be linked against in any number of languages (C# anyone? — @canti, I see you)
3. Node.js native addon module (same as the NPM package before)
4. Native Javascript implementation (slow, very slow, but it works)
5. WASM module for browser use (much, much, much faster than the Native JS in browser)

All of the builds support the core crypto used not only in wallet functions (creating keys, finding our outputs, generating ring signatures, etc) but they also contain all of the hash functions available in core, including Chukwa (Argon2id with our parameters). The WASM module makes it very easy to bring the crypto methods used in TurtleCoin to the browser which will make client-side web wallets faster than ever\*. In addition, if someone wanted to build a web miner based on the package they can do so.

_Spoiler alert: Someone is building a client-side web wallet built on this using wallet-backend-js._

**iburnmycd**

[turtlecoin/turtlecoin-cryptoTurtleCoin: Standalone Cryptography Library. Contribute to turtlecoin/turtlecoin-crypto development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-crypto)

![]({{ site.baseurl }}/images/0dy6pAIxZvV1FwLeb.gif)

**turtlecoin-utils**

Using the updates to the turtlecoin-crypto library, I’ve performed a few updates on the development branch of turtlecoin-utils. Most notably, the utils package now smart loads the crypto module. If we can load the Node native addon module, that’s always our first choice. If we’re in browser, then we try to load the WASM first. Lastly, if all else fails, we fall back to the native Javascript implementation. This also has the added benefit of cleaning up a bit of the code that revolves around the crypto in the library.

In addition, due to the exposure of all of the crypto functions in the library now, we’re able to check that the ring signatures that are generated via the library are checked to be valid upon creation thereby reducing the chance of generating an invalid transaction via the library.

If that wasn’t enough, I’ve added a webpack configuration to the project that ties everything up into a nice bundle for inclusion for browser use. Browser use did you say? You betcha. This webpack has been deployed as part of the TurtleCoin Explorer and is used for the tools page (playing with wallet addresses & keys) and the transaction checker. It’s going to make that top secret client-side web wallet shine.”

**iburnmycd**

[turtlecoin/turtlecoin-utilsNode.js utilities for working with the TurtleCoin network - turtlecoin/turtlecoin-utilsgithub.com](https://github.com/turtlecoin/turtlecoin-utils)

![]({{ site.baseurl }}/images/0Udv1trz0T8P3he2J.gif)

**CS-TurtleCoin**

Over the last week, I have done a lot on the CS-TurtleCoin/CantiLib project. I pushed some major updates, including a full rewrite of the main repo, which features improvements across the board. As I have been fairly silent with the project lately, I’m going to give a quick run-down of what it is and what I have gotten done thus far.

CantiLib is a multi-purpose C# library with many useful tools for a blockchain environment, including a standalone P2P client system, a configurable REST API server, logging utilities, database functionality, cryptography, byte-level serialization, and CryptoNote protocol handling. CS-TurtleCoin is an effort to tie these tools together to create a fully operational TurtleCoin node, coded from the ground up in a C#.

As of the time of writing this, I have P2P connectivity, API handling, CryptoNote deserialization, peer discovery and handshaking, some database functionality, the start of a blockchain cache, and a number of other utilities and functions in place. Lately, my focus has been on refining peer discovery between nodes, porting cryptographic functions from the core code to C#, connecting TurtleCoin-Crypto to the library, adding more functionality and ease of use to the API server, and have also begun work on the sync process and blockchain caching. More to come soon!

**canti**

[turtlecoin/cs-turtlecoinLive repo for TurtleCoin daemon spec and PoC. Contribute to turtlecoin/cs-turtlecoin development by creating an account…www.github.com](https://www.github.com/turtlecoin/cs-turtlecoin)

![]({{ site.baseurl }}/images/0er2bc6ym4OBIK17g.png)

**wallet-api-go**

**wallet-api-go**

This project aims to provide a wrapper for making wallet-api requests with Go. All of the wallet-api responses are marshaled into an appropriate type. You no longer have to manually convert from `map[string]interface{}`!

If there’s any bugs in the codebase, feel free to leave an issue on GitHub. :D

**dsanon**

[https://github.com/anonanonymous/wallet-api-go](https://github.com/turtlecoin/wallet-api-go/) <https://godoc.org/github.com/anonanonymous/wallet-api-go>

![]({{ site.baseurl }}/images/06DhJpt_VIdPfU_Vg.png)

**TurtleCoin Chukwa Cuvée Testnet available**

As everything is in full swing to get ready for the Argon2id-based new TurtleCoin algo called chukwa, we needed to spin up a local testnet.

This allows us to benchmark, test and optimize our different boards, and see how the trtlrig works compared to the native TurtleCoin miner.

We made our test environment available. If you want to see how your harware will do on the new algo, and try out how it feels living on the cutting-edge technology, build your trtlrig from the add_chuwka branch available in the TurtleCoin github, and point your xmrig miner using the following parameters:

`-o publicnode.ydns.eu:42333`  
`-a chukwa`  
`-u your TRTL address`

Please note no web front-end available, and no TurtleTestCoin pay-outs. This environment is for benchmark tests only.

@**OléCuvée**

![]({{ site.baseurl }}/images/0xiGH9Okt1KTvQrGK.gif)

34 hot singles in your area are waiting to upgrade your wallet format

**Wallet format upgrading**

A few people have requested that there be a utility to upgrade a wallet from the WalletGreen format (zedwallet, turtle-service), to the WalletBackend format (zedwallet-beta, wallet-api).

I’ve been working on this for the past few days, and think I am close to completion. Got a few bugs with transfer amounts being incorrect, but hopefully it won’t be a sticking point.

I’m considering adding an automatic upgrade, so you can transparently open an old format wallet and have it upgraded without any user interaction. One downside is that we have to generate the key image for each input when we upgrade the format, which is pretty slow for a large wallet — this can take around 10–20 seconds on my \~8000 transaction wallet.

Of course, this will only have to be done once, so the delay could be worth it.  
Hopefully this will make it easier for services to migrate to wallet-api, along with new GUI’s/CLI’s using the new backend.

**Zpalm**

## Rig Of The Week

Each week we like to highlight a person who has sent in pics and descriptions of their TRTL mining rigs. This week is ZenMaster Mr Lahaye’s turn! Ironically, it was his idea to start this column about rig of the week so maybe he had this planned all along! hmmm!

![]({{ site.baseurl }}/images/0hgFfJmXFbvbp9nC9.jpg)

![]({{ site.baseurl }}/images/0YQsflfMK_7NrpNjm.png)

![]({{ site.baseurl }}/images/0kPWf95zTZ--8I-Uc.jpg)

**RigRX560** by ZenMaster (MrLahaye)

6 x Msi Aero rx560 4GB with fan upgraded to Artic Accelero Mono plus  
1 x CPU Intel G3900 2.8Ghz  
1 x 8 gig DDR4 stick of memory  
1 x Msi z270-a pro Motherboard  
1 x Corsair 850 Watts powersupply  
1 x SSD Sandisk 16 GB with HiveOS  
1 x Veddha 6 Gpu mining rig Frame as pictured no fans

- Around 20 Kh/s
- This rig consumes around 350 Watts taken at wall.
- I got this complete rig for 600$ CAN on Ebay. Check Ebay auctions often and snipe last minute deals. I can usually get one or two deals like this every month.

I’ve already described myself in a previous roundup : <https://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-may-7-2019/>

![]({{ site.baseurl }}/images/0BwCjG6tx7zsEZQ5i.png)

## Advertisements

- CuvéeTurtle Pool located in the heart of Europe (Prague), with fast connectivity and scalable hardware platform (ARM-based SBC Cluster) is looking for you — miners like you of all shapes and sizes! Help us with our journey to grow our pool. You would still be one of our early adopters. Low payout limits. Our long-term commitment and friendly support by @Olé Cuvée himself. Pool web frontend webpage: [https://publicnode.ydns.eu](https://publicnode.ydns.eu/) Join us now! Point your miner to `publicnode.ydns.eu:5555 ./xmrig -a cryptonight-turtle -o 192.168.99.254:3333 -u TRTLxxxxxxxxx --donate-level 1 -p rig2`Flood us with some serious hash rate :) No matter how much you throw at us, we will cope with it! [https://publicnode.ydns.eu](https://publicnode.ydns.eu/)
- @shelly has finally started creating drawings and paintings for sale versus doing doodles for all of us Turtles. A few of her pieces are available at Buckland Arts. Can you spot which ones are hers? Check out the page and give it a like to support creative Turtles. <https://www.facebook.com/bucklandarts/>
- Browser miner, use it or embed it into your sites and let others use it! Hashes about 200–400 on mid setting. <http://turtle.japakar.com/miner>

## Buy With TRTL

These are things that were pinned this week in the `#merchandise` section of TRTL Network Discord [chat.turtlecoin.lol](http://chat.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0CavGJzWg2tWwZCIC.jpg)

selling asus dual gtx 1060 for 1.25M TRTL shipped (OBO) — ExtraHash on Discord

![]({{ site.baseurl }}/images/0oFBN2otyfpf9GA1L.JPG)

ASUS X370 CROSSHAIR VI EXTREME (full package) — 2M TRTL shipping within EU on quote — Elkim on Discord

![]({{ site.baseurl }}/images/0opdA6JLF8zj4QnnX.jpg)

I have brand new, still sealed GPU risers for sale in TRTL. 25k trtl each, 5 for 100k. opened this one to take a pic. Bulk quantities are available. Small amounts can be shipped for around 80k trtl in a flat rate padded envelope within the US. — ExtraHash on Discord

![]({{ site.baseurl }}/images/07Vp37SbTVvwdQNkL.jpg)

I have two clusters of RPis. 3 B+. Four in each cluster. 120 watt charging power supply. 2 each 5 port switching hubs. SD cards pre-programmed with Ubuntu and XMrig miner. All set to mine. Just connect to a router or range extender. Edit the config.json file with your wallet address. Good to go! If anybody wants this as a whole, make me an offer. I do not want to part this out. Comes with all 1 ft and 18" CAT 5e cables. Anyone interested? — RadarLarry on Discord

## Good First Issues

Trying to get your developer role in Discord? Want to be part of the dev team? Here are some ‘Good First Issues’ so you guys can have some low hanging fruit to get you started! Beginners, enjoy!

- QueryBlocksDetailed does not populate transaction extra “raw” property in response  
  <https://github.com/turtlecoin/turtlecoin/issues/815>
- Remove no longer relevant asserts  
  <https://github.com/turtlecoin/turtlecoin/issues/811>

## Shoutouts

![]({{ site.baseurl }}/images/0wuQOnOHzvjGQrXEU.png)

grey’s pi3b cluster of doooom

- iburnmycd Shoutout to @shelly for a successful grand opening of Buckland Arts where some of her artwork is featured.
- JAPAKAR KING OF THE OZARK Once again, shoutout to a great community! This place is unique and awesome!
- greywolf thanks much to DatsunPatrol for the Optimizing-RPi-TurtleCoin-Mining guide, and to Olé Cuvée (aka LeoCuvée) for the encouragement and oversight, as i put together a 4-raspi3b+ mini-tower mining TurtleCoin
- rock shout to zpalm for helping with my golang homework, thanks to dsanon for the wallet-api-go work, thanks to japakar, greywold, mufalito and others for tips this week, and thanks to the community for again being awesome, and thanks to teacup for the memes :D

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-june-17-2019/)_._
