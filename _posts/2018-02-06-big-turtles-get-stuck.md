---
layout: "post"
title: "Big Turtles Get Stuck!"
description: "To put it in simple terms, there’s an issue we’re running across out in the wild and figured it would be best to get ahead of it and keep…"
image: "{{ site.baseurl }}/images/1IhzJF_QYbHzwBfCAD8UdFw.jpeg"
date: "2018-02-06T22:44:42.749Z"
---

_To put it in simple terms, there’s an issue we’re running across out in the wild and figured it would be best to get ahead of it and keep the community aware of what is going on, and a possible solution while we address the issue._

![]({{ site.baseurl }}/images/1IhzJF_QYbHzwBfCAD8UdFw.jpeg)

A whale-turtle struggles to rebroadcast his transaction.

We’ve noticed that sending large transactions (2,000,000+ TRTL) can sometimes get a little hairy, because your wallet will notify both sides of the transaction that a transaction has been broadcast, but the transaction never gets confirmed, or included in a block. This ends with the transaction getting stuck, and after 1–21 days, cancelling.

## Normally this is fine.

In Bitcoin and other networks, these stuck funds return to your wallet after some days of not being processed, (they never really left), and you’re able to resume spending. In our case, however, and at least when it has happened to me, the funds remain stuck, and then when the transaction cancels, the wallet software still interprets these funds as attempting to be double-spent, like a US dollar hot off the photo-copier machine.

**What’s the problem?**

When someone creates a transaction with qualities that make it unsuitable to be processed, it cannot be included in a block easily or quickly. Similar to bitcoin, if you send a large amount of coins with no fee or very little fee, they can sit in the transaction pool until blocks expand to fit the extra size of the transaction into a block.

# **A good rule of thumb is to use 100 TRTL fee for every 1,000,000 TRTL you send,** . If you’re sending less than a million, a fee of 10 or less is fine.

## What’s The Solution?

For now, if you have to send a large transaction, split your transaction up into a few chunks of 500,000 TRTL, and if you don’t need the extra transactional privacy, you’ll increase your luck of not getting stuck by using a 10+ mixin for now until a fix is released. Confirmation time is fast on the network, there is no reason to send a large amount of coins all at once and expect it to clear easily.

**_For the nerds, or people who enjoy a more technical assessment of the situation:_** <https://github.com/forknote/cryptonote-generator/issues/54>
