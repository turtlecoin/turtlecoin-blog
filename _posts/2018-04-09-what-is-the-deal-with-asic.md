---
layout: "post"
title: "What is the Deal with ASIC?"
description: "While we talk about algorithm changes, I wanted to give some detail to TurtleCoin users about what’s happening now, what’s coming soon, and…"
image: "{{ site.baseurl }}/images/1AnX2woBwjcPRxdH54tlrZQ.png"
date: "2018-04-09T22:41:10.665Z"
---

![]({{ site.baseurl }}/images/1AnX2woBwjcPRxdH54tlrZQ.png)

## While we talk about algorithm changes, I wanted to give some detail to TurtleCoin users about what’s happening now, what’s coming soon, and what that means for everyone involved.

ASIC miners have hit the market, and various manufacturers are publicly offering a selection of Cryptonight and Cryptolight miners, purpose-built to efficiently and quickly mine coins on networks like ours. As soon as we heard the news, we issued a statement in a TurtleCoin Meta Forum post that talked about the importance of fairness for miners on the TurtleCoin Network.

[Take Your Baikal and Shove It Up Your ASICASICs are on the way; what does this mean for the TurtleCoin Network?medium.com](https://medium.com/@turtlecoin/take-your-baikal-and-shove-it-up-your-asic-b05c96187790)

The purpose of this post is to explain what we are doing to keep mining competitive, and to keep the community up to date on current efforts in this direction. As time and progress allows, I’ll be updating this article with new information, so be sure to bookmark it!

# Let’s talk about our options.

As with all matters, there are many options to choose from, and in our case, we have two: Do we accept ASIC on our network, or do we begin an ongoing effort to exclude them? Let’s take a minute to think hypothetically about what each option might be like.

![]({{ site.baseurl }}/images/12BD7MP34JwAo8sLZhCUtjQ.png)

![]({{ site.baseurl }}/images/1KRtUoX3Au3NEahNwFeOWxA.png)

Figure A. — a bad turtle

## What if we support ASIC?

One option is to change nothing, and adapt to a world with ASIC miners on our network. Their presence would offer an increase in network hash-power, a decrease in the orphaned block rate, less pressure on the GPU market, and a new wave of miners currently being excluded from other networks as other dev teams work fast to discourage ASIC compatibility.

**Let’s break that statement down, what does it _really mean_?**

- **_“ASIC would offer an increase in network hashpower”_**These machines are very effective at turning power into hash cycles, which means that as they board the network in greater numbers, the _difficulty_, or the amount of cycles it takes on average to unlock a block every thirty seconds goes up.
- **_“a decrease in the orphaned block rate”_**  
  If the global hash rate rises 20x as a result of the presence of ASIC miners, the probability that two miners reach the same solution in the same second is drastically less, as the granularity has increased greatly.
- **_“less pressure on the GPU market”_**If you’ve been shopping for GPUs recently, as a gamer, you probably noticed that prices have almost tripled since this time last year. As cryptoassets gained popularity around March 2017, mining hardware and GPUs had a surge of popularity and limited supply, as the same hardware is used by gamers and miners alike. ASIC has one purpose, hashing a single algorithm. They can’t run Crysis. When they’re done, they’re done.

![]({{ site.baseurl }}/images/1cWr-WYtzfpJ1xlIsakmA5w.png)

Figure B. — a good turtle

## What if we don’t support ASIC?

On the other hand, we can choose to keep mining fair and decentralized, we won’t have to take an oath of servitude to the chip manufacturers, we can still increase our network hash-power, and we will have many uses for our old hardware when it’s no longer profitable to mine with.

**Let’s unpack those statements:**

- **_“keep mining fair and decentralized”_**  
  ASIC manufacturers tend to be centralized in the same geographic area, with parts and resources produced sourced, designed and produced in-house. The potential for collusion or tampering with the flow of hardware from manufacturer to consumer is too high. This puts a single point of failure in front of too many parties that could have an interest in “squeezing” this market.
- **_“we won’t have to take an oath of servitude to the chip manufcturers”_**  
  When we, as a network, become dependent on a handful of chip manufacturers, all with similar interests, we can no longer make decisions that require consensus to enact. For example, if we decide to change our hashing algorithm to improve the quality of the network, and a hardware manufacturer doesn’t feel like re-tooling for this change, all they need to do is overpower everyone else on the network with hash-power that they’re in control of supplying to us, and there would be no upgrade taking place as a result. This relationship dynamic is unsustainable.
- **_“we can still increase our network hash-power”_**  
  Increasing the difficulty is a good thing for us, and in an algorithm change to eliminate ASIC, we are afforded an opportunity to deviate from our current hashing algorithm to a faster one that spins at a faster rate. This speed increase allows less risk of orphaned blocks.
- **_“many uses for our old hardware when it’s no longer profitable for mining”_**  
  ASIC hardware is good for a short amount of time before it becomes cost prohibitive to mine with. There is a regular upgrade cycle to keep up with production and difficulty. When your miner is no longer profitable, there is no resale value, and nothing inside the machine to be used for parts. When difficulty rises enough, you have a heater that generates 30 cents per year. GPUs can be resold, used for gaming, password hashing, 3D rendering, video production, and all types of research needing high amounts of number crunching power.

# Is ASIC The Only Problem We Can Solve?

Another issue we face is related to the orphaned block issue we spoke about above, rented hash-power. Networks like NiceHash and botnets currently have the ability to cause timing issues on our network. They immediately dump a load of hash-power on the network, and parallel orphan chains start getting created. The increase in hash-power outpaces the difficulty and miners reach the correct result on block after block simultaneously, and sometimes ahead of schedule.

This has many concerns and frustrations attached to it. Some people even look at it as further securing the network, but regardless of which side you’re on, if the network is emitting blocks out of schedule, the reward suffers, the schedule suffers, and it can’t be good for the consistency of transactions for the normal user.

We’ve decided that while we’re at the drawing board, we may as well come up with a multi-faceted solution that addresses everything. If we can somehow make ourselves incompatible with ASIC as well as rented hash-power and botnets, we can give power back to the miners who are investing in our network by running rigs at home.

![](https://miro.medium.com/max/3350/1*isZ9I28wMc-8gLzKxn9Uew.png)Stage One: In Testing Now!

# We’ve Got A Plan, And We’re Stickin’ To It!

The plan for tackling this two part problem is a two part response, and we’d like to take care of both. This is our plan currently in action for dealing with these issues.

> GPU Mining gives an incentive to the development team to always act in the best interest of and maintain a good standing with the community. At any moment miners have the option to go somewhere else.

## Stage 1: Algorithm Change 1

The first priority is to get out of the way of the biggest threat to the network, which is ASIC. If we don’t get rid of ASIC first, we may not have the ability to regain consensus to make further changes to our hashing algorithm for any further changes.

**We have several requirements for this stage:**

- _We must get out of the path of ASIC as fast as possible_
- _We must communicate and dedicate our support to pools and services in the transition_
- _We must have compatible mining software for users_
- _We must improve the consistency of blocks to reduce orphans_

In other networks, as we’ve seen, a rushed algorithm change can cause much disruption, as it has had no time to be tested for completeness and correctness, and hasn’t had time to be properly integrated in pools and services. While these things are fun to play with, we know that this is people’s money and time, and we must treat their resources with respect.

![]({{ site.baseurl }}/images/1yPNVlCRo6AZohXKCctqNjw.png)

# The option that fulfills each of these requirements, and still allows for immediate integration to pools and services is CN-Lite Variant 1

Below is a short point-by-point response to the previous concerns mentioned above.

- _We are able to implement these changes quickly and effectively, in accordance with the ASIC avoidance timeline_
- _We have support for pools and services out of the box, and are able to easily patch those that don’t._
- _We already have compatible mining software, most mainstream Cryptonight mining applications have patches tested and ready for this transition._
- _CN-Lite Variant 1 spins faster than the mainstream CN variant alternative, which helps prevent orphans, since we have such a short block target interval._

# What Is The Status Of This Change?

Currently, we are in Stage 1, with the new algorithm already in testing on our Testnet repository which you can review on GitHub currently at the link below.

[GitHub.com/RockSteadyTC/Testnet-V2Testnet for CN-Lite Variant 1 algo on TurtleCoin Networkgithub.com](https://github.com/RocksteadyTC/testnet-v2)

Community member Suml Noether is credited with making the upgrade change, and continues to add support and improvements to the needs of the network, like an improved node-multi-hashing library, which is an essential part of running a pool with the new algorithm. Here are links to the associated contributions:

[Added auto-switching to the new algorithm during the fork. by sumlnoether · Pull Request #6 ·…I recommend forking the node-multi-hashing repository referred in packages.json to an officially supported turtlecoin…github.com](https://github.com/turtlecoin/turtle-pool/pull/6)

[Add support for Cryptonight v6, Cryptonight-Light v0 and their variant 1 versions. Add block major…GitHub is home to over 20 million developers working together to host and review code, manage projects, and build…github.com](https://github.com/turtlecoin/turtlecoin/pull/119)

[turtlecoin/node-cryptonote-utilContribute to node-cryptonote-util development by creating an account on GitHub.github.com](https://github.com/turtlecoin/node-cryptonote-util)

[turtlecoin/node8-multi-hashingnode8-multi-hashing - Forked to provide Windows compatibility. Works on Node 8+github.com](https://github.com/turtlecoin/node8-multi-hashing)

I asked Suml to contribute a quote for this article, and got this in response:

> One morning I shot an elephant in my pajamas. How he got in my pajamas, I don’t know. — Suml Noether, 2018

For those of you that want to get in on the discussion leading up to Stage 2, please see my updated main post and the related GitHub discussion in the TurtleCoin Meta Forum post linked below.

[ASIC Resistance, TurtleCoin Hashing Algorithm Change · Issue #74 · turtlecoin/metaCredit to @ZedPea for bringing this to my attention. It has come to our attention that there are credible claims of an…github.com](https://github.com/turtlecoin/meta/issues/74)

Stay tuned as this article takes shape over the coming weeks. In the mean time, enjoy the testnet, and have a great week!

![]({{ site.baseurl }}/images/1Cp5ZKNX_rAREXscKiSu5Xw.png)

UPDATE April 9, 2018: The fork went by without errors. All is well. Bummer. Maybe TurtleCash next time :(
