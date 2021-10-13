---
layout: "post"
title: "Oh shit, I think it’s dead"
description: "For 27 minutes the TurtleCoin blockchain was dead on the table. We shouted at it, poked it with sticks, it was muerto.. Difficulty went from a healthy 2 Billion-ish area to 1, not 1 Billion, but 1, a…"
image: "{{ site.baseurl }}/images/0YMaslc-OftVciUPO.png"
date: "2019-08-30T02:39:54.601Z"
---

![]({{ site.baseurl }}/images/0YMaslc-OftVciUPO.png)

_For 27 minutes the TurtleCoin blockchain was dead on the table. We shouted at it, poked it with sticks, it was muerto.. Difficulty went from a healthy 2 Billion-ish area to 1, not 1 Billion, but 1, a single digit._

**What went wrong? What does this mean?**

First, you’re reading this because we’re back online and working. Rest assured everything is fine. We were down for less than half an hour and stayed in touch with services the entire way. Had this gone any worse, you’d be reading this story from the back of a milk carton.

## The difficulty with difficulty

Difficulty is the part of mining that makes sure that whether there’s 1 person mining, or 100 million people mining, that blocks stay difficult enough for a miner to solve so that we crack one every 30 seconds. Sometimes it can be 15 seconds, sometimes it can be 45, but as long as it averages 30 seconds over a few day’s worth of blocks, everything is fine.

> Our difficulty algorithm is LWMA2, by Zawy12\. This algorithm is suitable for networks of our size to keep our block difficulty smooth of spikes in the graph. It uses a moving average based on the blocks that came before the current one being mined to keep a constant adjustment of this difficulty factor so that no matter how many miners join us, all blocks come out as close to 30 seconds as possible.

Normally our difficulty algorithm works just fine, however during fork upgrades, especially ones that will radically change our hashrate, we have to make a best guess ahead of time of where we’ll be before, during and after fork hashrate wise. In this case, our test scenarios told us the difficulty adjustment we chose was good, but as with all things, running in production was a different story.

![]({{ site.baseurl }}/images/0xvdR2olwlgN_WT9a.png)

You can see the actual shit hitting the fan right here.

**7:51 PM** We first knew something was up, the first 11 blocks on the new algorithm came immediately, and difficulty immediately dropped to 1.

**7:56 PM** We had formed a plan and had an upgrade in the works when we realized what had happened. At this time we notified in **#announcements** on discord that there was a momentary delay and to stay tuned for a patch. Major exchanges and block producers were also notified.

**8:03 PM** We began tweeting the situation live after a mad scramble to find the login credentials. Not a single complaint was received during the delay, which was absolutely wonderful.

![]({{ site.baseurl }}/images/0BoWL1hT9TGVCo8Ew)

Only a single exchange responded to our advisory. Their response time was 3 minutes.

**8:12 PM** A patch is submitted and being built by CI on github to produce binaries. The source is released as 0.18.1 for others to build on their own while CI builds.

![]({{ site.baseurl }}/images/0Zy3e2o-mIIQUaXAy)

Wait a minute… did he merge without waiting for CI/CD tests to finish?!

**8:14 PM** Patch seems to work, we begin passing it on via Twitter and Discord to users. To bring some light to the situation we adopt the hashtag **#BorkedFork**

**8:15 PM** At this time we’ve received no complaints and only a single exchange responded to our message, which they responded in 3 minutes (Thanks TO, you’re a real one). We hold our breath and wait for the block producing (read: really big) pools to pass enough blocks to make it official.

**8:33 PM** Things have been going smooth enough at this point that we feel we can say we’ve revived the network and things are currently humming along at a blistering 159MH.

Well done everyone. You all helped each other to relay the correct information regarding the patch and we all made it through this small stumble.

This likely won’t be the last time we’ll go through this but a lesson learned is a lesson earned and we won’t be letting go of what we were taught tonight for quite some time. Thanks everyone who participated, especially IBMCD for providing the patch like a champ in just minutes. Bravo, all of you.

**TurtleCoin® Core Team**

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/oh-shit-i-think-its-dead/)_._
