---
layout: "post"
title: "This Week In TurtleCoin (May 28, 2019)"
description: "In this episode we made it to the papers when over 50,000 system administrators were found to be incompetent (hey ma!) In other news, water also wet. If you’d like to submit your dev update to the…"
image: "{{ site.baseurl }}/images/0TKB6Lg-9tJkkQYIX.gif"
date: "2019-05-30T05:16:52.223Z"
---

![]({{ site.baseurl }}/images/0TKB6Lg-9tJkkQYIX.gif)

In this episode we made it to the papers when over 50,000 system administrators were found to be incompetent (hey ma!) In other news, water also wet.

![]({{ site.baseurl }}/images/0AixHi7ZXpVeuasiv.gif)

**On the bright side, Home Depot is hiring all positions**

## Developer Updates

If you’d like to submit your dev update to the roundup, fill out this form <https://goo.gl/forms/BNaRYkUmOVOa1apQ2>

![]({{ site.baseurl }}/images/0du5S_rjuLYXvcYOR.gif)

**trtlrig**

**trtlrig**

Good news! I spent a bit of time over the holiday weekend and wired up the xmrig fork trtlrig to support Chukwa (Argon2id) CPU pool mining. I’ve tested it on Windows and a few different flavors of \*nix. @LeoCuvée also mentioned that he tested it on ARM. Overall, it’s ready to go but I’m sure that someone will come around and fine a few enhancements to squeeze a bit more hashrate out of it but it’s an awesome start.

[turtlecoin/trtlrigMonero (XMR) CPU miner. Contribute to turtlecoin/trtlrig development by creating an account on GitHub.github.com](https://github.com/turtlecoin/trtlrig/tree/add_chukwa)

**iburnmycd**

![]({{ site.baseurl }}/images/0LnphP-kKhWkAUDih.gif)

**node-turtle-pool**

**node-turtle-pool**

As part of testing trtlrig, I verified that all of the necessary updates for turtle-pool are complete for Chukwa. Everything needed has been merged into the development branch if you’d like to set up a testnet and pool for testing yourself.

[turtlecoin/node-turtle-poolMining pool for TurtleCoin. Contribute to turtlecoin/node-turtle-pool development by creating an account on GitHub.github.com](https://github.com/turtlecoin/node-turtle-pool/tree/development)

**iburnmycd**

![]({{ site.baseurl }}/images/0iXOUWVnOeMUNlRm9.png)

Successfull build and test of the Chukwa TRTLrig on SBC

**Successfull build and test of the Chukwa TRTLrig on SBC**

In the past few days, we managed compile and test the TRTLrig for the Argon2id Chukwa algo which TurtleCoin will fork to at block 1,800,000.

For our testing, we have used slightly different parameters than those that will be used by TurtleCoin (512kb memory, 3 iterations).

For our test, we worked together with @CapEtn of WRKZCoin, which will use 256kb memory and 4 iterations. Results?

Partly pleasing, partly requiring further optimizations.

The RK3328 chip that runs the Rock64 boards (which we use for our SBC nodes) gets a very nice bump. The increase is from underperforming slow 310 h/s on cryptonight-turtle to 550 h/s on Chukwa 256/4.

We also tested on the cryptonight-turtle best performer OrangePI One Plus, which is based on the Allwinner H6\. Unfortunately, we could not seem to get any increase in hash rate on Chukwa 256/4 for this board, quite the opposite.

The OrangePI One Plus that otherwise excells on cryptonight-turtle (750 h/s) and actually does less on chukwa 256/4, specifically 623 h/s, no matter what we tried so far.

Well, there is a room for improvement! Slow & steady!

**LeoCuvée#1481**

![]({{ site.baseurl }}/images/0Rj91x_R2y33Alg1B.png)

**Wallet sync speed improvements**

**Wallet sync speed improvements**

As mentioned last roundup, I planned on working on multi-threading the sync process for wallets. This has now been completed and merged, and has given some decent speed gains.

Wallet syncing should now scale up to the number of cores you have (Provided you’re using the latest code and either wallet-api or zedwallet-beta). We’re now bottlenecked solely on how fast we can retrieve blocks from the daemon. Because of this, we don’t see huge increases in speed — as most of the time, we’re just waiting for more blocks rather than using all our threads.

However, if you have a less powerful device that previously was CPU bottlenecked — For example, a raspberry pi or other SBC, this should result in some more significant speed improvements.

Unfortunately, when using a remote daemon, threading does very little in terms of increasing sync speeds. This is a good reason to run a local daemon, especially on an SSD, if you want your wallet to sync super quick!

As you can see from the image above, with 12 threads and a local daemon, you can sync a wallet with over 10k transactions in under an hour.

[Multithreaded wallet syncing by zpalmtree · Pull Request #821 · turtlecoin/turtlecoinMulti-threads the wallet syncing progress. Threads are configurable via command line option. I have encountered a…github.com](https://github.com/turtlecoin/turtlecoin/pull/821)

**Zpalm**

![]({{ site.baseurl }}/images/0oohcVTNi6nLgv1jI.gif)

**turtlecoin-crypto**

**turtlecoin-crypto**

Some advancement has been made on the stand alone crypto module that includes all of the necessary code in a nice, tight, static library for performing any crypto/hash related functions used within the Core project.

1. Implemented a wrapper that passes all data into and out of the methods as strings to make it easier to link up to the library instead of having to carry a whole bunch of structs around.
2. Added Chukwa support
3. Improved Windows build process so that it creates a shared library (.dll) with the export definitions defined so that it can be linked against by other projects “easily”. See #dev_canticore for it’s first use (when he’s ready).
4. Working to combine all of the turtlecoin-crypto repos (JS/Node.js/WASM) library builds into a single repo.
5. Much, much, more.

[turtlecoin/turtlecoin-cryptoTurtleCoin: Standalone Cryptography Library. Contribute to turtlecoin/turtlecoin-crypto development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-crypto)

**iburnmycd**

![]({{ site.baseurl }}/images/0eXKPMxUfRYQsjFFB.gif)

**turtlecoin-multi-hashing**

**turtlecoin-multi-hashing** **& turtlecoin-cryptonote-util**

Again, to support trtlrig & pool testing for Chukwa, the Node.js turtlecoin-multi-hashing & turtlecoin-cryptonote-util packages heavily used by pools and the like have been updated to support Chukwa (Argon2id). This package has been published to NPM and GitHub and is ready for widespread use.

[turtlecoin/node-cryptonote-utilContribute to turtlecoin/node-cryptonote-util development by creating an account on GitHub.github.com](https://github.com/turtlecoin/node-cryptonote-util)

[turtlecoin/node8-multi-hashingForked to provide Windows compatibility. Works on Node 8+ - turtlecoin/node8-multi-hashinggithub.com](https://github.com/turtlecoin/node8-multi-hashing)

**iburnmycd**

![]({{ site.baseurl }}/images/0KBFAaCJX-aS3sVR4.jpg)

**Dockerized TurtleCoin with TTYD**

**Dockerized TurtleCoin with TTYD**

I recently came across a cool program called TTYD that shares a terminal with the web and decided to integrate it into my docker projects. I initially started with TurtleCoind and, after realizing how easy easy it was, quickly moved on to zedwallet. Once those two were completed I was able to create a docker-compose file that spun up both services on the same network, allowing you to view the TurtleCoind output and interact with zedwallet via a browser. At this point I was kind of taken with TTYD and decided to start containerizing some of the other terminal based community projects using this new (to me at least) shiny toy.

Words don’t really do this any justice. If you’re familiar with Docker and want to see it in action, jump to the run commands down below. If, on the other hand, you’ve been pushing off learning Docker, never understood what the hype is about, or never heard of it? Stop right now and go download it [here](https://docs.docker.com/install/#supported-platforms). Seriously, go do it, I’ll wait. And while you’re at it install [Docker Compose](https://docs.docker.com/compose/install/#install-compose) too. In the meantime, I’ll gush about some of the things that I think makes Docker cool.

Docker containers are standardized so we don’t need to worry about our environment, like finding and installing the right libraries on our host machine, to get the software up and running. They are portable and reusable in the sense that they can be easily pulled, started, stopped, or removed when needed (which is great for trying out new software). We can run multiple containers and allow them to communicate and share data with each other over isolated networks. We are able to mount files/folders located on the host within our containers which makes development easier. The list goes on, but enough of my fanboying let’s get started.

Now that you have Docker installed let’s spin up a container that runs TurtleCoind. Open up your terminal and run:

`docker run -d -p 7681:7681 -p 11897:11897 --name turtlecoind-ttyd -v turtlecoind:/home/turtlecoin/ andrewnk/turtlecoin:turtlecoind-ttyd`

Now access [http://localhost:7681](http://localhost:7681/). After a few moments, you should see a terminal pop up and the familiar output of the TurtelCoind daemon.

But what about zedwallet, you say? Try it out with this command:

`docker run -d -p 7682:7681 --name zedwallet-ttyd -v turtlecoind:/home/turtlecoin/ andrewnk/turtlecoin:zedwallet-ttyd`

Then access [http://localhost:7682](http://localhost:7682/).

Pretty cool, right? Using this setup we won’t be able to actually use zedwallet though, because we haven’t provided a node for it to connect to. Before moving on, remove both containers we just created, by running the command:

`docker rm -f turtlecoind-ttyd zedwallet-ttyd`

Using Docker Compose we are now going to run both containers connected to each other on an isolated network and accessible via the browser.

First you need to save the file that contains the “instructions”, then use docker-compose to spin everything up. Download this [docker-compose.yml](https://raw.githubusercontent.com/andrewnk/turtlecoin-docker/master/docker-compose/turtlecoind-zedwallet-ttyd/docker-compose.yml) file and save it as docker-compose.yml. Then in your terminal navigate to the file and run:

`docker-compose up -d`

Once everything is up and running you can navigate to [http://localhost:8080](http://localhost:8080/) to see TurtleCoind and to [http://localhost:8181](http://localhost:8181/) to use zedwallet. You are now running the daemon and can use zedwallet as you normally would. In this instance all the data (TurtleCoind and zedwallet files) will be stored in a folder, created by the containers, on your host machine titled turtlecoin.

When you’re done playing you can destroy the containers and network by running:

`docker-compose down`

This is just a quick overview of what can be done. Each image can accept a wide array of variables to customize your container.

So far, I have created TTYD images for:

- miner
- Turtle CLI py
- Turtle Network CLI
- TurtleCoin Test Suite
- TurtleCoin Wallet NodeJS (Divine)
- TurtleCoind
- TurtleCoind HA
- zedwallet

Check out the repo at: <https://github.com/andrewnk/turtlecoin-docker>

If you have any questions, are interested in contributing, or have a suggestion for another dockerized community project then hit me up on discord.

[andrewnk/turtlecoin-dockerDockerfiles and docker-compose files to run various TurtleCoin software and projects - andrewnk/turtlecoin-dockergithub.com](https://github.com/andrewnk/turtlecoin-docker)

**andrew | trtl.rocks**

## Rig Of The Week

If you’d like to submit your rig to Rig Of The Week, send us your info here: <https://goo.gl/forms/GkDSoP3fERBWm8aJ2>

![]({{ site.baseurl }}/images/0zPB2SExpEktplfG2.jpg)

**Home mining**

_Describe this rig! Give us as much detail for your post as possible._

13 amd video cards — 7970 rx550 rx570 rx580

_What are your secret tips and tricks about mining TRTL?_

Ubuntu, xmr-stak/xmrig, ask in discord and forums, read all the stuff ppl have to say in answer, then read everything else everywhere. to the nvidia fans: theres a ‘better than equivalent’ with 2gpus on my AMD cards. lol imho lol

_Introduce yourself_

Started mining as hobbyist . Want to get better result through mining

_What is the hashrate of this rig?_

115 khs

## Bounty Watch

Bounties are a great way for motivated people to get things done! To submit your bounty, click here: <https://goo.gl/forms/mkNv27sJtv1nHPtx2>

![]({{ site.baseurl }}/images/0RRuoDeoIr4o8-YcN.gif)

**Bounty: Chukwa (Argon2id) GPU Miner Support**

**Bounty: Chukwa (Argon2id) GPU Miner Support**

Requirements: — Add GPU mining capabilities to any open source miner package with Pool support — Must support, at minimum, CUDA (NVIDIA) and all current OpenCL (AMD) cards including Vega — Must include benchmarking ability — Must include hash tests (see below for input and expected output) that complete successfully Acceptance Criteria: — Must meet the requirements above — Must be pushed to a **public** GitHub repository — Must honor all aspects of existing licenses — Must remain open source — Must pass tests on multiple GPU platforms Hint: You may find inspiration and/or basic support for hooking this up via <https://gitlab.com/omos/argon2-gpu> Input Data:

0100fb8e8ac805899323371bb790db19218afd8db8e3755d8b90f39b3d5506a9abce4fa912244500000000ee8146d49fa93ee724deb57d12cbc6c6f3b924d946127c7a97418f9348828f0f02

Expected Hash:

c0dad0eeb9c52e92a1c3aa5b76a3cb90bd7376c28dce191ceeb1096e3a390d2e

**2,000,000 TRTL**

**Contact RockSteady for further details.**

![]({{ site.baseurl }}/images/0xTwZJXSMgPou9HEM.gif)

**TREZOR HW WALLET community firmware**

**TREZOR HW WALLET community firmware**

What: Make a community Trezor firmware for Trezor One or T or both in order to store private keys safely, send and receive TRTL.

Why: We can’t have official integration merged in their master branch, however they suggested we can fork their code and make our own and first community Trezor firmware ever. In addition if that happens, they would like to promote it in media.

**3,500,000 TRTL**

**Contact Elkim for further details.**

![]({{ site.baseurl }}/images/0t0dcpUXhQCRvRGWm.gif)

## Community Advertising

Click here to submit your free ad: <https://goo.gl/forms/mkNv27sJtv1nHPtx2>

- Hey turtles, I created a new exchange featuring your favourite cryptonote coins: TRTL, DEGO and more coming. Create an account today and start trading. ;) — We’re still in beta phase — ping @fipsi in our Discord if something isn’t working — <https://discord.gg/xm4rfWF> [https://tradelly.co](https://tradelly.co/)
- CuvéeTurtle Pool located in the heart of Europe (Prague), with fast connectivity and scalable hardware platform (ARM-based SBC Cluster) is looking for you — miners like you of all shapes and sizes! Help us with our journey to grow our pool. You would still be one of our early adopters. Low payout limits. Our long-term commitment and friendly support by @Olé Cuvée himself. Pool web frontend webpage: [https://publicnode.ydns.eu](https://publicnode.ydns.eu/) Join us now! Point your miner to publicnode.ydns.eu:5555 ./xmrig -a cryptonight-turtle -o 192.168.99.254:3333 -u TRTLxxxxxxxxx — donate-level 1 -p rig2 Flood us with some serious hash rate :) No matter how much you throw at us, we will cope with it! [https://publicnode.ydns.eu](https://publicnode.ydns.eu/)

## Shoutouts

- greywolf thanks to oiboo for rush delivery of special wolfhair mane oil
- greywolf shoutout to zpalmtree for never sleeping, and for always keeping a finger on the pulse of every channel
- greywolf cheers for Sierra, who can always find the good in anyone, even the slimiest of worms
- Quicky Chech out new web wallet Trtlfun. <https://trtlfun.com/> Thanks
- greywolf i wanna thank RockSteady for mentioning possible porting of TurtleCoin to FreeBSD. it sparked an interest, and now i’ve got a running 12.0-RELEASE system with a working window manager :-)
- Dreday000 Shout to the community, Just want to say good job TurtleFam
- Elkim Thanks Oiboo for the awesome Hairy Turtle beard elixir!
- Rock Shouts out to Krebs on Security and Kaspersky for not smearing us too much in their latest articles. Shouts out to Kaspersky more though for actually spelling our name right though.. Also, special reminder to keep your systems up to date, lest you become what the Chinese call «_Les incompétents_»

![]({{ site.baseurl }}/images/09ixRh2_43Y0RC3_R.png)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-may-28-2019/)_._
