---
layout: "post"
title: "Running A Public Node For Fun & Profit"
description: "If you answered yes to all three of these, you’re a damn liar, but you’re also well qualified to be a public node operator! It’s easy and risk free. You might be thinking this is already over your…"
image: "{{ site.baseurl }}/images/048yswVzfEpmZn2yx.gif"
date: "2018-08-27T00:41:49.679Z"
---

## _A lot of people ask us about ways to make some extra TRTL on the side without fancy mining hardware or waiting for tips or bounties. We have your answer now, and we think you’re going to like how easy it is!_

![This Could Be You](https://miro.medium.com/max/856/0*48yswVzfEpmZn2yx.gif)

This Could Be You

- **Do you have a basic grasp of following step by step directions?**
- **Do you read an article instead of skimming it?**
- **Do you tend to Google the basic stuff first before bothering someone helping you?**

If you answered yes to all three of these, you’re a damn liar, but you’re also well qualified to be a public node operator! It’s easy and risk free. You might be thinking this is already over your head, but fear not. If you have synced the whole blockchain before on your home computer, then you already know how to do this.

## What is a public node?

A public node, or public daemon is a computer that a user can connect to safely and sync their wallet without downloading the whole blockchain at home. The node operator doesn’t know which wallet or who is connecting, and they also can’t see balances or passwords.

![Gucci Guwop, public node operator](https://miro.medium.com/freeze/max/60/0*5XfMxUxwTZNYGT6c.gif?q=20)

![Gucci Guwop, public node operator](https://miro.medium.com/max/1000/0*5XfMxUxwTZNYGT6c.gif)

Gucci Guwop, public node operator

## How do I use a public node to make money?

In the beginning, community members ran public nodes for free. This is a great thing to do for the community, but as with all things that are free, they do have a cost for someone, and can often be congested. Free nodes will still be allowed if someone wants to run one, but you can now set a per-transaction fee quite easily, for people who connect to your node. This guide will help you get a public node set up, and the fee is up to you.

> Free nodes can sometimes be busy because they get lots of users connecting to them. Nodes that charge a fee can sometimes offer faster service because not many are willing to pay a fee to send a transaction. A free market is emerging to allow nodes to set their own prices and let the community use the nodes that fit best for them.

## Is this a Masternode?

**No.** Masternodes are used in non-cryptonote networks to mix coins to make up for what they lack in native privacy. Every TRTL daemon mixes internally, automatically using Borromean Ring Signatures, so we have no need for Masternodes. Masternodes are a risk for privacy, and have nothing to do with what we are talking about in this article. **If someone told you that TRTL has Masternodes, then they likely don’t know what they’re talking about.**

> **Nobody can steal your password or use your information by running a public node, and you will not harm someone else if your node goes down. No worries!**

## **What you’ll need:**

1. **A computer with an IP address that doesn’t change.** _If you’re running it from home and use cable or DSL internet, you’re probably already set up with a static IP. (Free Amazon servers or Google Cloud servers are perfect for this)_
2. **A TurtleCoin wallet to collect your earnings.** _You can use a web wallet like_ [_https://Shellnet.pw_](https://shellnet.pw/) _for this or you can generate a paper wallet at_ <https://turtlecoin.lol/wallet> _— so long as you have the keys to the wallet, you’re ready to rock!_

## Let’s Get Started

1. **Connect to your node and install TurtleCoin.**  
   You can follow the compile guide on <https://github.com/turtlecoin/turtlecoin> or download a Release from [http://latest.turtlecoin.lol](http://latest.turtlecoin.lol/)
2. **Decide on a fee, and launch the daemon**  
   Let’s say I want to charge 500 TRTL per transaction sent, I can launch my daemon like this:  
   `./TurtleCoind --fee-amount **50000** --fee-address TRTLuxEnfjdF46cBoHhyDtPN32weD9fvL43KX5cx2Ck9iSP4BLNPrJY3xtuFpXtLxiA6LDYojhF7n4SwPNyj9M64iTwJ738vnJk`

**NOTE: I highlighted the amount 50000 because we said we were going to charge 500 TRTL per transaction, but I just typed 50000, so what gives? TRTL is only measured in “coins” to make sense to humans, but to the network, everything is measured in shells, which are 0.01 TRTL,** [**so for 500 TRTL, we need to charge 50,000 Shells, or “atomic units” as we call them.**](http://supply.turtlecoin.lol/)

## What Do We Do Next?

**Get your node listed** on Github and TurtleTurtle.org so that people know you exist!

- <https://github.com/turtlecoin/turtlecoin-nodes-json/blob/master/turtlecoin-nodes.json>  
  _This is a list we use to fetch data from all of the public nodes for displaying on pools and explorers. Putting your information here can mean free advertising on a lot of TRTL services._
- <https://github.com/turtlecoin/turtleturtle.org/blob/master/index.md>  
  _This is the community directory TurtleTurtle.org which is a website where every Turtle Service is free to list their TRTL site or project for other users to see._

## How Can I Get More Users?

Some people do a web frontend with stats, like [https://turtlenode.io](https://turtlenode.io/) or [https://turtlenode.net](https://turtlenode.net/) using IBMCD’s frontend software [https://github.com/turtlecoin/turtlenode.io ](https://github.com/turtlecoin/turtlenode.io)which shows the status and user load of each node you operate.

**Users love something they can look at, but they love uptime even more. In part 2 of this article, Iburnmycd will walk you through how to use TurtleCoind-HA, a program he made to monitor and restart your high availability node if it ever goes down or gets slow. Stay tuned!**

![Image result for haha business](https://miro.medium.com/max/60/0*svCr2SN3Vd3zHVL4?q=20)

![Image result for haha business](https://miro.medium.com/max/632/0*svCr2SN3Vd3zHVL4)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/running-a-public-node-for-fun-profit/)_._
