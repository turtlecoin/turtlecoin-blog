---
layout: "post"
title: "This Week In TurtleCoin (April 30, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0i1OJor8TVffMxWRl.gif"
date: "2019-05-01T03:06:37.076Z"
---

![]({{ site.baseurl }}/images/0i1OJor8TVffMxWRl.gif)

![This week we'd like to give thanks to the pizza guy for always being on time, and never forgetting the parmesan. You make this whole thing possible dude-friend-guy.](https://miro.medium.com/max/960/0*M_HZCq1buNXxYuS8.gif)

This week we’d like to give thanks to the pizza guy for always being on time, and never forgetting the parmesan. You make this whole thing possible dude-friend-guy.

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

To submit your link, click this link <https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform>

![]({{ site.baseurl }}/images/06aeH2Ac2u126QsPm.png)

.trtl Domain Name System

**Deploying global .trtl resolvers with docker**

Ok, been a while away, but as it is Winter now i think i can find some inside time, cold blooded and all that. I was excited to see the trtl resolver announcement and went to work straight away deploying them around the world onto 6 droplets globally.

I put together a Dockerfile that uses node:lts-alpine as ibmcd documentation is amazing as usual. I added some comments at the top of the file on how to build and run. The comments will assist in building the image, running the container and testing that the resolver can actually resolve by hitting it with a GET request using curl.

Not seeing much on my resolvers in the way of logs (apart from bots hitting the port looking for services that don’t exist, sneaky guys). Maybe i’m missing something, if anyone wants to do some tests or knows something i don’t know hit me up.

Looking forward to see what is going to develop out of this service, I’m sure it will make life easier for a lot of TRTLs.

This was a good task to get back into the game. I have another little project in the works also, so stay tuned for that. Another thing to make life a bit easier. Plenty to do in TRTL town. **— Slash-atello**

[turtlecoin/.trtl-resolverResolver implementation. Contribute to turtlecoin/.trtl-resolver development by creating an account on GitHub.github.com](https://github.com/turtlecoin/.trtl-resolver/blob/master/Dockerfile)

Divine — A TUI Wallet for TurtleCoin

**Divine — A TUI Wallet for TurtleCoin**

“I just began work on `Divine`: a TUI wallet for TurtleCoin utilizing node.js. I'm utilizing `wallet-backend-js` for the wallet operations and `blessed` for the terminal API. My goal is to make this a responsive, easy to use ""command line""-like wallet with full mouse support. Of course it will also be able to receive commands by keyboard as well.

I’d love for somebody to help me out with the ASCII art. If anybody can help let me know.” — **ExtraHash**

[https://github.com/turtlecoin/turtlecoin-wallet-nodejs](http://blog.turtlecoin.lol/%20https://github.com/turtlecoin/turtlecoin-wallet-nodejs)

![]({{ site.baseurl }}/images/05U4aoGu7SvIP6Sa1)

**turtlecoin-wallet-backend-js**

Been doing some work on the JS wallet backend this week. The main thing is that I’ve added fusion transactions. Extra has started making a wallet using the backend, which has given some valuable feedback on the docs, and other things, so thank you extra.

![]({{ site.baseurl }}/images/0r351qPcPKonCrk9M.gif)

I’ve also started work on adding an auto optimize feature, which will keep your wallet fully optimized with no input from you or the wallet developer — it will automatically send fusion transactions whenever needed to ensure you’re always good to go. Of course, this can be disabled, if the developer wants to handle optimization themselves.

On another note, I’ve been looking at the feasability of rewriting TonChan in Qt with C++. This will of course take quite a while, but may eek out a bit of syncing performance. It seems there’s a large performance loss from passing data from JavaScript, to J\*\*\*, to C++, and back again, in the realm of 10x. Or, I’m doing something stupid. ¯\_(ツ)\_/¯  
So far I’ve stripped out all the code aside from everything needed for the C++ WalletBackend. That sounds like an easy job.. but takes an age when everything is linked to a huge module, and you have to shuffle stuff around.  
Anyway, that’s done, so hopefully I can try compiling it into a library I can chuck into a Qt app, and can get some initial numbers on sync speed, so I can tell if this is worth persuing.” **Zpalm**

![]({{ site.baseurl }}/images/0vOGw6qpH-N9Nkbtc.png)

Awesome TRTL

**Awesome TRTL**

Created a simple list of all the live .TRTL domains I could find.  
Please do a pull request if you created something on a .TRTL domain” **— Turtle Max**

[mrrovot/awesome-trtl🐢 Awesome list of .TRTL domains. Contribute to mrrovot/awesome-trtl development by creating an account on GitHub.github.com](https://github.com/mrrovot/awesome-trtl)

## Rig Of The Week!

**Rackmount SBC Cluster**

![]({{ site.baseurl }}/images/0nAEIskrASg8BjXR0)

![]({{ site.baseurl }}/images/0UrlLAWAvKiaBxrSj)

![]({{ site.baseurl }}/images/0oEcJOw6veNz9HgKJ)

![]({{ site.baseurl }}/images/0cZuZtrPrfIY960y2)

![]({{ site.baseurl }}/images/0RKkoLEfzl6VJbdz2)

There are 14 NanoPi Fire3 boards in the front row with 10 OrangePi One+ boards in the second row. Six fans are situated at the front of the rack and blow air past all the boards. The boards use hexagonal standoffs for positioning and are also supported by the ethernet cables on the bottom that feed through the plexiglass.

Try to be mindful of power consumption if you can. I mainly view TRTL as a hobby mining project with some good potential upside but I think its important to be mindful of energy consumption nevertheless.

I am a low-power computing enthusiast and a fan of ARM architecture Approximately 24 kh/s give or take. Each NanoPi Fire3 produces about 1.2kh/s and each OrangePi is producing about 700 h/s. I’m hoping to optimize hashrates more in the future as more stable OS options become available for the OrangePi boards.

_Submitter didn’t include a name, if you’d like your name up here, just let us know in the chat and we’ll get you credited. -rock_

## Bounties!

![]({{ site.baseurl }}/images/08pKGTtgCRnTpd1bH.gif)

- 4/8/2019 23:00:19 100 “I am Offering a Bounty of 100 TRTL if you add a ‘Pay with TRTL’ button to your website (just 2 lines of code)
- I’ve been working on <https://trtlbutton.com/>, it lets you generate a button and accept TRTL on your website by copying just 2 lines of code! You can check out a demo of a simple html page with 2 lines of code here: [https://trtlbutton.surge.sh](https://trtlbutton.surge.sh/)Feedback is welcome!” Turtle Max /@mrrovot (github)
- 4/13/2019 5:36:45 100 so nice Tomáš
- 4/21/2019 18:02:06 100,000 Adding TRTL support for TrustWallet <https://github.com/TrustWallet/wallet-core/blob/master/docs/Contributing.md#pull-requests>tps @SpoofytheWhale
- 4050000 “Trezor T and turtle-services integration

_What_: Integrate popular hardware wallet from SatoshiLabs, Trezor T with Trezor’s backend and turtle-services in order to create and encrypt, decrypt wallet and sign transactions with the device.

_Why_: Trezor T is fully open-source hardware wallet project with it’s own responsible-disclosure program. As hard as it is to get added into Trezor’s frontend app wallet.trezor.io, one of the unofficial requirements is to have Trezor integrated in project’s application first.

We might have a guy who would do it so here comes a softcap for the job:

Soft-cap: 10 000 000 TRTL

+1 000 000 from @Elkim | trtl.urmom.lol

- 2 050 000 from @TurtlesHill
- 1 000 000 from @LeoCuvée | cuveetrtl.czech.cloud | cuveetrtl.czech.cloud

Total: 4 050 000 TRTL” Elkim

## Community Advertising

- Turtle Pool with Loki Merge Mining from HashVault.pro <https://turtle.hashvault.pro/en>
- TRTLint provides a free API for converting a Turtlecoin address and a payment id to an integrated address. Our HTTP API is easy to use and free for all types of projects, including commercial ones. Made by @fipsi | The Machine <http://trtlint.de.cool/>
- Live in Maryland? Need a 6card open air case? I’ve got one for free. Not shipping cause I just don’t feel like taking it apart. DM Mining4Vets on discord. Need gone asap. Case is one in back with red fans. MINING HARDWARE NOT INCLUDED
- Hands on your hips about extortionate TX fees? Turtlenode.online strives to provide a reliable and affordable public node service you can trust. You can find it in all reputable GUI wallets; look for the node with a 4.2 TRTL fee and that’ll be public.turtlenode.online. The node operator would like to thank everyone for their continued support!

## Shoutouts & Thanks

![]({{ site.baseurl }}/images/0kxBWTpAFkpZhPbSc.gif)

Happy birthday Alien :D

- Ksmith1532 Want to give a shout out to @pstarSR#7761 @wll1rah#6816 for helping me with my endless questions with fixing my mining problems. #turtlepower
- zerouan thanks to teacup for trying to get a skateboard graphic
- zerouan thanks to grey for the pixel to inches to dpi conversion
- greywolf cheers to oiboo, who always comes in to start the day off with lots of happiness
- roger alien, go shill turtlecoin on the ETN discord for some attention.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-30-2019/)_._
