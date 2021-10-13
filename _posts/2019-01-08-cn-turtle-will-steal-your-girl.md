---
layout: "post"
title: "CN Turtle Will Steal Your Girl"
description: "With all the commotion about the next fork upgrade, and the debut of our new hashing algo, CN Turtle, I wanted to make sure everyone has the run down about the fork upgrade before it arrives in a few…"
image: "{{ site.baseurl }}/images/0XPX1GxhaYuP8n7pg.gif"
date: "2019-01-08T04:51:44.902Z"
---

![]({{ site.baseurl }}/images/0XPX1GxhaYuP8n7pg.gif)

With all the commotion about the next fork upgrade, and the debut of our new hashing algo, CN Turtle, I wanted to make sure everyone has the run down about the fork upgrade before it arrives in a few weeks. Today, I got with IBurnMyCD who has been the lead on this algo and got a short interview about what is CN Turtle and what does it mean to me, both as a miner and a user.

If you’re a miner, a user, or a fan of fine rewritable optical media, I think you’ll enjoy this article. It was a fun interview. If you have any questions, just click this link and join us in the chat, we’re all here waiting on you.

![]({{ site.baseurl }}/images/0Sqw3qENCUaVXh5K-.gif)

We’re all gonna make it

## RockSteady

@iburnmycd thanks for taking the time to do this interview. I wanted to get with you to discuss the upcoming fork upgrade in simple terms so our users know what’s in store for them.

First, what is the deal with this fork upgrade and why are we doing this?

iburnmycd

Thanks for having me @RockSteady (TRTL). It’s always an honour to help let the community that isn’t in the Discord all the time to catch the latest and greatest news. A while back, the project made the commitment to the community that the project would do its best to remain mineable for as many users as possible. Part of holding to that commitment is investigating, testing, implementing, and upgrading the Proof of Work used by the project. We’ve done this with experimenting with CN Soft Shell that a few forks of TurtleCoin have implemented and again with CN Turtle that we’re forking to at block 1,200,000\. This upgrade is designed to help keep the project mineable for everyone by reducing the resource requirements necessary to mine. As a result, everyone will see higher hash rates which also means that there is a higher chance of solving a block as each miner will be producing hashes noticeably faster. However, there will be more hashes required (on average) to find a block. Our hope is that in the larger scope of things, this works out to be a win for the the littlest miners.

## RockSteady

You mentioned our miners will be mining faster, what does that translate to for someone who has 100H/s of CPU power or another person who has 100H/s of GPU power?

## iburnmycd

Based on testing, we estimate that miners will see on average an increase of anywhere between 3.0x and 4.0x for CPUs and 2.0x to 3.0x on GPUs. Personally, on my hardware I’ve observed a 3.8x increase on my CPU (AMD 1950x) and 2.8x on my GPU (AMD Vega64). However, not every CPU and GPU performs the same so the increase may be more or less than what we’ve observed. Variations in drivers, the mining software used, etc may result in higher or lower increases; however, what we can all agree on is that miners will see an increase in hashrate, no matter how small, due to the lower resource requirement and iteration count. On average a miner who was seeing 100H/s on CPU may see approximately 350H/s and a miner seeing 100H/s on GPU may see approximately 250H/s after the upgrade takes effect.

## RockSteady

That’s great news. Let’s say you’re a miner, what do you need to do to be ready? Are most major miners already ready to work? And what if you’re just a user, do you have to do anything?

## iburnmycd

That depends on how you mine :) If you’re a solo miner and you use the miner binary distributed with the project, you’ll need only upgrade to v0.12.0 once it’s released. The miner software will automatically switch to the new PoW algorithm when it’s time. If you’re mining with a pool, you’ll need to contact the pool operator or check their website to verify that they have upgraded their pool software for the upgrade. If they haven’t, you might want to give them a gentle reminder that they need to do so. In addition, you’ll want to make sure that you have the latest release of your favorite mining software. For instance, we’ve released the necessary updates for xmr-stak via trtl-stak (<https://github.com/turtlecoin/trtl-stak/releases/latest>) that has the updated algorithm available as `cryptonight_turtle`. In the coming weeks, we'll submit a pull request to the main xmr-stak repo to support the change. We're still working the kinks out of the automatic algorithm switch in the package but in the event we don't work that in, a miner need only manually switch the algorithm, delete their CPU & GPU configs, and let the software do the rest. We're still working on adding support into XMRig and hope to have that completed before the network upgrade. We've also received information that SRBminer has also implemented the algorithm. Users of that mining software will need to switch the algorithm over when it's time. Everyone, miners or not, need to keep their eyes out for the v0.12.0 release of the project. Service Operators, home users, pool operators, and other services will need to upgrade to v0.12.0 well ahead of block 1,200,000 to be ready for the upgrade. For most users, this upgrade will be like any other upgrade that we've done where you drop the new version in and you're good to go.

## RockSteady

Whats the best way to see how long we have before the upgrade takes effect?

## iburnmycd

The quickest and fastest way is to head on over to the official block explorer at <https://explorer.turtlecoin.lol/> In the _Network Stats_ area, you’ll see an area that says **Next Network Upgrade In (est.)** with the approximate number of days, hours, minutes, and seconds until the next network upgrade.

![]({{ site.baseurl }}/images/0KB1yXtghdmJdElDI)

## RockSteady

Thanks for taking a second to tell us about the fork upgrade, is there anything else you wanted to add?

## iburnmycd

If you’re reading this and you are not on Discord, you should be. We’d love to have you. It’s the only way to get a real feel for the project and meet all the different personalities. If you want to help out, there’s plenty of different areas to check out from development, education, marketing, international groups, and everything in between. Discord is the best place to meet other cryptocurrency developers who share a passion for the technology and their projects. Besides, where else can you learn about codename Chukwa?

## RockSteady

Thanks

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/cn-turtle-will-steal-your-girl/)_._
