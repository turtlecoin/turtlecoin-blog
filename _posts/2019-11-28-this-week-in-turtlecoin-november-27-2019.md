---
layout: "post"
title: "This Week in TurtleCoin (November 27, 2019)"
description: "This week we tightened up our turkey gravy recipes as well as our core software while we reflected on how thankful we are to have such a talented community. Read on to find out more! This is a place…"
image: "{{ site.baseurl }}/images/0vLk2TqD4axIQrLS_.jpg"
date: "2019-11-28T01:33:13.881Z"
---

![]({{ site.baseurl }}/images/0irLnxXAB6xtp2CJn.png)

This week we tightened up our turkey gravy recipes as well as our core software while we reflected on how thankful we are to have such a talented community. Read on to find out more!

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

![Image result for revenge of the nerds](https://miro.medium.com/max/60/0*vLk2TqD4axIQrLS_.jpg?q=20)

![Image result for revenge of the nerds](https://miro.medium.com/max/1400/0*vLk2TqD4axIQrLS_.jpg)

Have you ever had a calculator on your belt clip? Of course not, because you haven’t won a crypto hackathon yet. Where’s the next crypto hackathon, you say? Well buddy, we’ve got you covered.

## **TurtleCoin Crypto Hackathon 2019**

We have 15 Million TRTL looking for a new home, and have 24 teams so far who’ve signed up for the TurtleCoin Crypto Hackathon 2019 (Signups open until December 1), and so far of those 24, 9 have left their details to be contacted during the hackathon for an article about their projects. That’s a great turnout, and a surprisingly even balance between devs and non-devs.

[TurtleCoin Crypto-Hackathon 2019To celebrate our 2nd year as a community on December 9th 2019, we are sponsoring the first annual TurtleCoin™…crypto-hackathon.com](https://crypto-hackathon.com/)

**We are excited to thank the following teams for their participation:** _ZenTurtles, Why Canti Think of a Team Name, Hero’s in a Half Shell, MobileTortile, Lord_Enzo, that turtle, Kurdîstan, Born without a shell, Spanner Pouch, Hashterisk, AMC, JS TRTLz, TeamXenth, hebeblock, E Squad, Kick Ass Turts, Psychotic Silverfish, MXZ, Save the Turtles, eyegenvalue, termek, Oiboo Games, Double-O-Seven, ninja_

**Raw blocks syncing**

This week I’ve been working on adding raw block syncing to wallets. So far I’ve just added it to zedwallet and wallet-api. Currently, when syncing wallets, the daemon collects blocks and transactions from the database, deserializes it, and dumps it out to JSON. The wallet then parses that JSON and processes the blocks.

With this patch, the daemon instead returns the unparsed, raw blocks from the database as JSON. We then perform the deserialization in our wallet, and then process the blocks.

The advantage of this is two-fold. The first one is that generally wallets are waiting on the daemon to supply more data, rather than busy processing blocks. This new RPC call is a lot faster to complete than the current one, and so when the daemon is serving lots of wallets, it means that the wallets will spend less time waiting to retrieve data, and more time processing blocks, which means faster sync times.

The second advantage is that the raw blocks are much more compact than the full block data in JSON, so data usage will be decreased.

The next step is to add this feature to the JS backend so TonChan and Proton can benefit from it.

**Zpalm**

**TonChan v1.0.2**

Small TonChan release going out today. It fixes a bug where you were unable to sync past a particularly huge block.

Also fixes a bug with node swapping when you changed screens before the node swap completed.

Finally, it fixes QR codes not populating the amount to send correctly in some scenarios.

As always, you can view the full set of changes on GitHub: <https://github.com/turtlecoin/turtlecoin-mobile-wallet/compare/v1.0.1…v1.0.2>

**Zpalm**

![]({{ site.baseurl }}/images/0gEiGmjGbN0wJ5oRH.gif)

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**Service Operator** — Miner.rocks, zhang

**Reporter** — Khorosho!

**Tester** — rollinghavoc

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- Use matches property in ApiDispatcher regex #862  
  <https://github.com/turtlecoin/turtlecoin/issues/862>
- Remove no longer relevant asserts #811  
  <https://github.com/turtlecoin/turtlecoin/issues/811>
- Utilise /getblocks and client side serialization for faster syncing #54  
  <https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/54>

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

![]({{ site.baseurl }}/images/0KyQPwadKzvwCLDb5.jpg)

Anton — Simple raspberry pi mining cluster 2.4KH/s

## Bounty Watch!

This is an easy way to make a few TRTL!

**50,000** “Make a TurtleCoin Christmas Themed Logo! This will be used for the discord server icon. The deadline is the 30th November, 11:59pm GMT.

To see more details, and the entries so far, check out the pinned message in the #bounties channel in discord.” **zpalm**

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- Hello. My name is Kevin, owner of SpookyPool.nl. My goal with SpookyPool is to create a great community with fun people and having a nice chat about crypto and other stuff. Having TurtleCoin in my pool since a while ago has been fun. Learned alot of new things and meet alot of new people. I would like to ask u to join the community of SpookyPool by mining TurtleCoin or some other currency! [http://trtl.spookypool.nl](http://trtl.spookypool.nl/)
- Please support the muxdux turtlecoin mining pool — Active Discord with great people, very low pool and tx fees, great hardware infrastructure [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- Japakar pneumonoultramicroscopicsilicovolcanoconiosis
- Japakar Thanks all to the community as always! You guys are great!
- Turtley McTurtleton McDrizzle Hi there!
- japakar.com You guys are awesome! Vury nice. She is my sister.
- rock thankful that we spent this year together

## and one last thing..

Earlier today, the question was asked in the Discord chat what everyone was thankful for this year. We said we’d publish them on the roundup, so here they are, in no specific order.

![]({{ site.baseurl }}/images/0f9KsotyDevB8iLQ7.png)

![]({{ site.baseurl }}/images/0hucKty3uIsaTEVe1.png)

![]({{ site.baseurl }}/images/0u0Bp-FHB9m9mrocu.png)

![]({{ site.baseurl }}/images/0f2tTS2_kzi9lLkll.png)

![]({{ site.baseurl }}/images/03xmi4jWEfTrZxMRA.png)

![]({{ site.baseurl }}/images/0Y6df7iAVsEOo53PL.png)

![]({{ site.baseurl }}/images/0X7eJK7xUnXFa-B5P.png)

![]({{ site.baseurl }}/images/0ct8eoKyQ9Rzk6yhy.png)

![]({{ site.baseurl }}/images/0zad328wOSLdLpHzB.png)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-november-27-2019/)_._
