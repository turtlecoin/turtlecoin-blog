---
layout: "post"
title: "Let’s Talk About Mixins"
description: "We are moving to static mixins, and we want to talk to you about what those words mean and why that’s important for your privacy."
image: "{{ site.baseurl }}/images/1dWtQjTgNMHL6lQiBk_CvUA.gif"
date: "2018-07-11T00:11:21.010Z"
---

## We are moving to static mixins, and we want to talk to you about what those words mean and why that’s important for your privacy.

![](https://miro.medium.com/max/3200/0*3JbvQxdCxwJmuPZS)In this diagram, Linda privately sells a half ounce of donuts to Debra.

![]({{ site.baseurl }}/images/16pQt0IFTX6Z6y2WF3RLlgg.png)

## In the beginning…

In the days before Cryptonote, there were coin mixing operations for Bitcoin users to hide the origin of their coins. The mixer would be a web app that shuffled bits and pieces of Bitcoin back and forth enough where it became slightly more difficult to figure out who sent what. Aside from being the perfect recipe for exit scams, these days, with companies like Chainalysis and the non-fungible nature of Bitcoin, this does very little to enhance privacy.

The way mixing is done with TurtleCoin currently, is that the network basically files the serial numbers off the coins first before the mixing is done. This shuffling happens internally, for just about every transaction, which prevents this type of analysis. This mixing is based on a concept called _Borromean Ring Signatures_, which was first written up by Blockstream, a Bitcoin company.

[Blockstream/borromean_paperborromean_paper - Technical paper on the Borromean ring signature constructiongithub.com](https://github.com/Blockstream/borromean_paper)

## The current state of mixins

Right now, for every transaction a user can set a mixin number. Someone who uses a mixin of 0 sends their transaction without any benefit of privacy. This can sometimes be a from the misguided assumption that the transaction will cost less, or go faster, but this isn’t true. [Using a mixin of 0 can even hurt the privacy of those around you.](https://lab.getmonero.org/pubs/MRL-0004.pdf)

Conversely, there are some users that swear by a mixin of 420, 710 or whatever their preferred lucky number is. It’s not any benefit to mix to this extent if you talk about it openly and everyone else isn’t also mixing to this degree. You could end up being a victim of “tall poppy syndrome” and your transactions would be fairly easy to pick out of the flock.

## What is the solution?

In the next fork at block height 620,000 we will be switching to using only mixin 7, and the mixin level is no longer user definable. The benefit of this, aside from everyone using a good amount of mixing, is that if everyone is using the same number, it becomes harder to pick any one transaction out of the crowd and say “that transaction came from XYZ exchange because they only use mixin 17 to commemorate the year they incorporated,” etc.

The drawbacks of this are few- transactions might take a split second extra to be mixed, and pools or services who miss the upgrade date might not be sending valid payments until they do. None of this impacts the average user in a negative way, and the entire network benefits as a whole.

![]({{ site.baseurl }}/images/1dWtQjTgNMHL6lQiBk_CvUA.gif)

A group of TurtleCoin users mixing happily ever after

## The path forward

The goal for mixing in future upgrades is pretty simple. We plan to gradually raise the mix level with each upgrade cycle until things begin breaking or something better comes along. There are other networks currently employing the same strategy who are using higher static mixins successfully, so we don’t foresee any issues and are reasonably confident the upgrade to 0.6.3 should go smoothly.

Pools and users should upgrade before 620,000, and for the most part everything should go smoothly. We’ve reduced the dust threshold to 0 ahead of this change, which means you can spend your wallet down to your last penny shells to ease this transition.

**Please contact your pools and services to ask if they’ve upgraded!**

# Don’t forget to upgrade! Here’s a link to the latest!

[turtlecoin/turtlecointurtlecoin - TurtleCoin is a private, fast, and easy way to send money to friends and businesses!latest.turtlecoin.lol](http://latest.turtlecoin.lol/)
