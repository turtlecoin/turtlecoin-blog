---
layout: "post"
title: "We’re Under Attack.. Here’s what’s happening, and how you can help."
description: "The network is being hit with small denial of service attacks. Nothing is at risk, or being destroyed, it’s just annoying, and we need your…"
image: "{{ site.baseurl }}/images/1GeFxORcnM19RDbR6EyadLQ.gif"
date: "2018-05-10T07:48:37.953Z"
---

![]({{ site.baseurl }}/images/v0.5.0)

## The network is being hit with small denial of service attacks. Nothing is at risk, or being destroyed, it’s just annoying, and we need your help to stop it.

## Whats the attack?

By spamming small transactions with lots of tiny inputs and high mixins, someone is knocking daemons offline that can’t handle the mixing of such a high number. Mainly it is affecting pools and public nodes. Windows daemons don’t seem to be affected. Linux and Mac daemons may see an increased number of segfaults.

> **NOTE: Your TRTL is fine**, nobody is stealing anything or breaking the network, it’s just momentarily annoying for pools and services to have to keep restarting their daemons every time they’re knocked down.

## What is the solution?

**Short-term solution:** We need your help. [Download today’s update](http://latest.turtlecoin.lol/). You can help defend against the attack by running the patched [TurtleCoin v0.5.0 ](http://latest.turtlecoin.lol/)daemon, which disables these types of malicious transactions that don’t fit the normal profile of a regular user on the network. The patch in the code will attempt to go live on the network at block #440,000, and that’s why we need as many people updated as possible, so the transition goes smoothly.

**Long-term solution:** Ideally, we _want_ to be able to mix ridiculous transactions and keep rolling. We need bug reports, logs, dumps, screenshots so we can help do more than just put a bandaid on what type of transactions we validate. Our daemon software has its own flaws, and we are working hard every day in public to fix them, and if we could be better optimized to handle mixing transactions like this, we could fix the problem without excluding any transactions, and without inviting disruption. Consider this, maybe the attacker is saying “hey man, fix your stuff!”, they’re right!

## **When does the patch become active?**

This patch affects the way the network validates transactions with ridiculous mixins going forward, so we need as many people updated to v0.5.0 as possible before we hit block 440,000, which is about 12–18 hours from the time of this article.

## How do I upgrade?

**Go to** [**http://latest.turtlecoin.lol**](http://latest.turtlecoin.lol/) **and download the file appropriate for your system, and drag your wallet files over to the new upgraded version’s folder after you unzip it.**

That’s it! You’re updated! Run the new daemon, check out our new cool ASCII art when you launch, and pop in the chat to let us know that you’re helping to fight the good fight with us. [http://chat.turtlecoin.lol](http://chat.turtlecoin.lol/)

![]({{ site.baseurl }}/images/1FXjVeo9S2Iiuidyvln0vfA.png)

**Thanks for reading, and thanks for helping!**

**❤ Rocksteady**
