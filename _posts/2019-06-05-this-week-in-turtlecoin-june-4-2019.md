---
layout: 'post' 
title: 'This Week In TurtleCoin (June 4, 2019)' 
description: 'As mentioned last week, I’ve been working on combining the different versions of this repo together. Good news! It’s done. 1) A c++ static library (Windows, Linux, OSX)
2) A shared library via DLL…' 
image: '{{ site.baseurl }}/images/0Gz7ma882ljsc2bZ7.jpg' 
date: '2019-06-05T02:40:32.033Z' 
---

![]({{ site.baseurl }}/images/0Gz7ma882ljsc2bZ7.jpg)

![Image result for stock photo](https://miro.medium.com/max/1400/0*i8ar5qdODP44ak5K.jpg)

Then he said “It’s pronounced ‘sah-joe’, the 8 is silent.”

## Developer Updates

![]({{ site.baseurl }}/images/016uXek_m7EYH84Mn)

Just when you thought this shit couldn’t get any more unintelligible

**turtlecoin-crypto**

As mentioned last week, I’ve been working on combining the different versions of this repo together. Good news! It’s done.

This repo now builds the following:

1. A c++ static library (Windows, Linux, OSX)
2. A shared library via DLL (Windows) that can be linked against in any number of languages (C# anyone? — @canti, I see you)
3. Node.js native addon module (same as the NPM package before)
4. Native Javascript implementation (slow, very slow, but it works)
5. WASM module for browser use (much, much, much faster than the Native JS in browser)

All of the builds support the core crypto used not only in wallet functions (creating keys, finding our outputs, generating ring signatures, etc) but they also contain all of the hash functions available in core, including Chukwa (Argon2id with our parameters). The WASM module makes it very easy to bring the crypto methods used in TurtleCoin to the browser which will make client-side web wallets faster than ever\*. In addition, if someone wanted to build a web miner based on the package they can do so.

Spoiler alert: Someone is building a client-side web wallet built on this using wallet-backend-js.”

**iburnmycd**

[turtlecoin/turtlecoin-cryptoTurtleCoin: Standalone Cryptography Library. Contribute to turtlecoin/turtlecoin-crypto development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-crypto)

![Image result for robot human](https://miro.medium.com/proxy/1*fdmBZ0WC0INf3w8sogbK6w.jpeg)

sajo’s github bot :D

**TurtleCoin Github Bot**

I’ve been looking into supporting multiple people making an issue at once with the Github bot; it doesn’t seem like it’ll be too hard to add, and it’ll be a nice little perk. If you don’t know what the Github bot is, I recommend you check it out! It lets you easily create a Github issue on any turtlecoin repo w/out an acc; type “!tag issue” in the #bots channel to learn more

**Sajo8**

![Image result for stock photo](https://miro.medium.com/max/60/0*nenkwQvwZLsXJEJ_.jpg?q=20)

![Image result for stock photo](https://miro.medium.com/max/1400/0*nenkwQvwZLsXJEJ_.jpg)

exile-bot

**turtlecoin-utils**

Using the updates to the turtlecoin-crypto library, I’ve performed a few updates on the development branch of turtlecoin-utils. Most notably, the utils package now smart loads the crypto module. If we can load the Node native addon module, that’s always our first choice. If we’re in browser, then we try to load the WASM first. Lastly, if all else fails, we fall back to the native Javascript implementation. This also has the added benefit of cleaning up a bit of the code that revolves around the crypto in the library.

In addition, due to the exposure of all of the crypto functions in the library now, we’re able to check that the ring signatures that are generated via the library are checked to be valid upon creation thereby reducing the chance of generating an invalid transaction via the library.

If that wasn’t enough, I’ve added a webpack configuration to the project that ties everything up into a nice bundle for inclusion for browser use. Browser use did you say? You betcha. This webpack has been deployed as part of the TurtleCoin Explorer and is used for the tools page (playing with wallet addresses & keys) and the transaction checker. It’s going to make that top secret client-side web wallet shine.

**iburnmycd**

[turtlecoin/turtlecoin-utilsNode.js utilities for working with the TurtleCoin network - turtlecoin/turtlecoin-utilsgithub.com](https://github.com/turtlecoin/turtlecoin-utils)

![Image result for stock photo](https://miro.medium.com/max/60/0*pXAPKsnEPKgVVL3l.jpg?q=20)

![Image result for stock photo](https://miro.medium.com/max/1000/0*pXAPKsnEPKgVVL3l.jpg)

tfw your db corrupts twice in the same day

**CS-TurtleCoin**

Over the last week, I have done a lot on the CS-TurtleCoin/CantiLib project. I pushed some major updates, including a full rewrite of the main repo, which features improvements across the board. As I have been fairly silent with the project lately, I’m going to give a quick run-down of what it is and what I have gotten done thus far.

CantiLib is a multi-purpose C# library with many useful tools for a blockchain environment, including a standalone P2P client system, a configurable REST API server, logging utilities, database functionality, cryptography, byte-level serialization, and CryptoNote protocol handling. CS-TurtleCoin is an effort to tie these tools together to create a fully operational TurtleCoin node, coded from the ground up in a C#.

As of the time of writing this, I have P2P connectivity, API handling, CryptoNote deserialization, peer discovery and handshaking, some database functionality, the start of a blockchain cache, and a number of other utilities and functions in place. Lately, my focus has been on refining peer discovery between nodes, porting cryptographic functions from the core code to C#, connecting TurtleCoin-Crypto to the library, adding more functionality and ease of use to the API server, and have also begun work on the sync process and blockchain caching. More to come soon!

**canti**

[turtlecoin/cs-turtlecoinLive repo for TurtleCoin daemon spec and PoC. Contribute to turtlecoin/cs-turtlecoin development by creating an account…www.github.com](https://www.github.com/turtlecoin/cs-turtlecoin)

## Rig Of The Week

[Hashrate of the BarracudaPost with 2 votes and 107 views. Shared by KirkRefund. Hashrate of the Barracudaimgur.com](https://imgur.com/gallery/FcwjrP3)

Japakar’s Barracuda

**Specs**  
Ubuntu 18.04, XMR-Stak 2.7  
Intel® Celeron® Processor G540 2M Cache, 2.50 GHz  
Hashrate about 230h/s.  
MSI ms-7680 Motherboard, 4gb Memory DDR3 SDRAM, Expansion Slots PCI Express x16, PCI Express x1.

**Secrets**
To mine on just about anything and everything you can, because you can always use more TRTL. I am Japakar, I mine on just about anything and everything. I love lamp, and TRTL.

**Hashrate** 230h/s

![Image result for advertising meme](https://miro.medium.com/max/60/0*StLMbToywWLOEStP.jpg?q=20)

![Image result for advertising meme](https://miro.medium.com/max/1246/0*StLMbToywWLOEStP.jpg)

## Community Advertisements

- Hey turtles, I created a new exchange featuring your favourite cryptonote coins: TRTL, DEGO and more coming. Create an account today and start trading. ;) — We’re still in beta phase — ping @fipsi in our Discord if something isn’t working — <https://discord.gg/xm4rfWF>
- FUCK EFNET -madk
- CuvéeTurtle Pool located in the heart of Europe (Prague), with fast connectivity and scalable hardware platform (ARM-based SBC Cluster) is looking for you — miners like you of all shapes and sizes! Help us with our journey to grow our pool. You would still be one of our early adopters. Low payout limits. Our long-term commitment and friendly support by @Olé Cuvée himself. Pool web frontend webpage: [https://publicnode.ydns.eu](https://publicnode.ydns.eu/) Join us now! Point your miner to publicnode.ydns.eu:5555 ./xmrig -a cryptonight-turtle -o 192.168.99.254:3333 -u TRTLxxxxxxxxx — donate-level 1 -p rig2 Flood us with some serious hash rate :) No matter how much you throw at us, we will cope with it! [https://publicnode.ydns.eu](https://publicnode.ydns.eu/)
- shelly has finally started creating drawings and paintings for sale versus doing doodles for all of us Turtles. A few of her pieces are available at Buckland Arts. Can you spot which ones are hers? Check out the page and give it a like to support creative Turtles. <https://www.facebook.com/bucklandarts/>

## **Shoutouts & Thanks**

- **Rock** Shoutout to phate and oiboo for working out a deal for the US people :)
- **Dreday000** Shout to the community, Just want to say good job TurtleFam
- **Elkim** Thanks Oiboo for the awesome Hairy Turtle beard elixir!
- **Japakar** Thanks everybody, you all are the coolest. :)
- **DroppingThePacketsHard**#0510 / TheDevMinerTV#9308 These people are wonderful, idea rich and lovely. Shoutout to all people that helped me to get accepted by Rock!
- **greywolf** thanks to ExtraHash for the ideas, and RockSteady for the live tech support, to help me get the gnome desktop environment for FreeBSD running.
- **iburnmycd** Shoutout to @shelly for a successful grand opening of Buckland Arts where some of her artwork is featured.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-june-4-2019/)_._
