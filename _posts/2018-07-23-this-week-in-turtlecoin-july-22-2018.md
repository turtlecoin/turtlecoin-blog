---
layout: "post"
title: "This Week In TurtleCoin (July 22, 2018)"
description: "This week we reached #27 on CoinGecko Developer Score, polished our golang skills, and compiled almost completely on Raspberry Pi!"
image: "{{ site.baseurl }}/images/085cE4WTIHgndBVms.png"
date: "2018-07-23T06:22:49.468Z"
---

## This week we reached #27 on CoinGecko Developer Score, polished our golang skills, and compiled almost completely on Raspberry Pi!

![]({{ site.baseurl }}/images/085cE4WTIHgndBVms.png)

Pictured: A sample of TurtleCoin legacy daemon code

# Announcements

A new fork upgrade has been released! In this release we moved the entire network up a notch on the security score and set a static mixin of 7\. [If you don’t know what that means, we have an article about it right here!](https://medium.com/@turtlecoin/lets-talk-about-mixins-430730035297)

If you use a local daemon, please upgrade your software to the latest version of TurtleCoin. If you run a service like a pool or faucet and haven’t upgraded yet, you’ll notice walletd is now called service. New users are easily fooled by the word “wallet” so until walletd is on it’s own in releases, we’ll be calling it “service”.

# Developer Updates

_These are updates from our open developer community. We like to hear about your project whether you’re done or not,_ [_so be sure to leave an update about your Turtle project for next week!_](https://goo.gl/forms/TQ1XoykWFpyVUxVO2)

![]({{ site.baseurl }}/images/0J3mlhNcxCbjxNHqp.jpg)

left to right: Canti, Rashed, Zpalm, Iburnmycd

**C# Daemon —** _Hihi\~\~ Canti has started some great work on the C# port of the daemon lately. I didn’t want to leave it all to him so I’ve been helping out a bit — so far I’ve ported the public/private key cryptography, so we can generate keys which will work as they do in the current daemon. I’ve also ported mnemonic seeds, and am now working on deriving addresses from public keys working. We would love some help, so if you are competent in C# hop over to #dev_general and maybe you can implement something too! Also — If you want to start working in another language, that would be cool too! Rashed has started work on the same stuff in golang — we’re really interested on getting daemon’s implemented in multiple languages, so if one has a bug, the whole network doesn’t crash._ **— Zpalm**

[ZedPea/CantiLibCantiLib - A general purpose library for crypto shenanigans.github.com](https://github.com/ZedPea/CantiLib/tree/master/CantiLib/Blockchain/Crypto)

> **We would love some help, so if you are competent in C# hop over to #dev_general and maybe you can implement something too! Also — If you want to start working in another language, that would be cool too!**

![]({{ site.baseurl }}/images/0cKMpHYRwmJzY6CjW.PNG)

TurtleCoin OneClickMiner

**TurtleCoin OneClickMiner —**_Heyoo everyturtle! ;) Some weeks ago, I’ve written about the upcoming features for the TurtleCoin OCM and now the new version is finally out! Along with a ton of fixes, this new release comes with automatic saving of selections and settings and new help texts. I declared it a beta pre-release — if you encounter bugs or notice flaws, please let me know on Discord or GitHub! Thanks ^^_
_I’m looking forward to hearing from you!_ **— EncryptedUnicorn#7915**

[turtlecoin/one-click-minerone-click-miner - One click miner GUI for xmr-stak to specifically mine the Turtlecoingithub.com](https://github.com/turtlecoin/one-click-miner)

![]({{ site.baseurl }}/images/0sO12sED8ct3hbSM-.jpg)

Webwallet v2 (Work in progress)

**Webwallet v2 (Work in progress) —** _I started to create a new Webwallet with PHP using the Laravel Framework. It will be more stable, easier to use and more secure than the old one. It’s not finished yet._ **— cryptoBOOM**

![]({{ site.baseurl }}/images/0Y5yvdgqLGZsGRwpr.jpg)

**Athena ATHX Update** _— Block emission now requires 4 transactions to be in the queue before a block is created, ensuring that we operate with as little waste as possible. To my knowledge nobody else is doing this. Currently we are emitting one block per day on average. We’ll be beginning collaboration on a proof of stake whitepaper and implementation soon, along with an update article._ **— Rock**

[athena-network/athenaathena - Athena is a slow block settlement layer for other blockchainswww.github.com](https://www.github.com/athena-network/athena)

# Community Advertisements

_Would you like to promote your Turtle pool or service that you run? Advertise it here for free!_

![]({{ site.baseurl }}/images/0h9Wn3y0XILRiwniE.png)

- Hi as owner Turtle.Land I decided that I wanna make pool, Pool named Turtle.Casa is open for all of you… SSL port, Low fee, Payout on PayID supported, Config generator. Pool is hosted on Google Cloud server,

[Turtle.Casa - \[TRTL\] -Mining PoolEdit descriptionturtle.casa](https://turtle.casa/)

![]({{ site.baseurl }}/images/1CKUixbYxM77phFdA0ZMpZA.png)

- Hello, I would like to invite everyone to our mining pool! <http://turtleminers.club/> Turtle Miners Club is a premier mining pool. We regularly find blocks! Speaking of blocks, we just reached our 200 blocks! Come join the club as we head towards 500 blocks. NEWS! We lunched a new WEB CPU MINER. Use your web browser and CPU to miner TRTL!

[Crypto Webminer - Mining in your BrowserEdit descriptionturtleminers.club](http://turtleminers.club/pages/webmine/)

![]({{ site.baseurl }}/images/02_6NNuEpnXIVRnsZ.jpg)

- Hey all, just chiming in to let everyone know that snail races officially begin next Sunday. I am in the process of building a racetrack and wanted to remind everyone that we have our own TurtleCoin snail racing server linked here:

[Discord - Free voice and text chat for gamersStep up your game with a modern voice & text chat app. Crystal clear voice, multiple server and channel support, mobile…discord.gg](https://discord.gg/xUyS7Xm)

# Community Shoutouts

_Is there a person in the community who you’d like to mention in the roundup for being awesome? Go ahead and submit a shoutout!_

secret-fan#1111 — weekly reminder than kev, beary, xaz and bunny are awesome

Imperdin — Shoutout to RockStready for being the first one to pronounce Imperdin correctly!

anon — Thanks to all the dev Turtles and helpful folks for getting so many people into crypto on a deeper level. All the average joes in the discord have a much more developed understanding of how cryptocurrencies function because of your hard work. Massive accomplishment in itself

![]({{ site.baseurl }}/images/0b2bOBO6AvpLrURWn)

Dacus — sss

Dreday00 — Shoutout to my Turtlefam, the most intelligent and chillest community. Come and hangout, the water is nice ;)

Specter — Thanks to all the Dev’s who are working behind the scenes to make Turtlecoin something genuinely better and not just another meetoo coin.

Browns1964Champs — I would like to thank Roger for growing snails in his swimming pool.

deskpro1886 — github-github.com/DeadManWalkingTO/Windows10MiningTweaksDmW improves turtlecoin hashrate in windows worth trying out or you can try DoNotSpy10 or Easy Service Optimizer I have all these enabled to reduce background etc windows unnecessary programs .I hope when squirrel research acorn gpu accelerator does turtlecoin we get double or triple hashrate!!!

Boris — Keep on turtling!

Khem Boi — Turtle Turtle

secret-fan#1111 — Weekly reminder than kev, beary, xaz and bunny are awesome

secret-hater#2222 — shut up zpalm

funkypenguin — Sending some ❤ to Duplicity(https://geek-cookbook.funkypenguin.co.nz/recipies/duplicity/), backer-upper of critical files, which avoided loss of data after my datacenter storage platform melted last week. The NZ TRTL pool is back in action again, at <https://trtl.heigh-ho.funkypenguin.co.nz/>

rashedmyt — Huge shoutout to dsanon for fixing critical bugs in my go wrapper.. forgot to mention him in the last week roundup

rashedmyt — Thanks a lot to zpalmtree for helping me out with the keccak port in go

tjwmagic — Shout out to CodIsAFish for lending a helping hand!

Roger Robers — Shout out to the whole world, TurtleCoin is the shiznit!

Zpalm — Shout out to luigi1111 from Monero for his amazing website — <https://xmr.llcoins.net/addresstests.html> — it’s awesome for checking you’re programming things correctly when messing with private keys, mnemonics, addresses, and more.

Zpalm — Play doki doki literature club\~\~, it’s free on steam
