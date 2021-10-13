---
layout: "post"
title: "This Week In TurtleCoin (July 7, 2020)"
description: "This week we protested peacefully against the lives wasted coding in lesser languages that don’t rhyme with poo-basic and argued for a solid hour about the color of a single dot on a page nobody…"
image: "{{ site.baseurl }}/images/0uQSfqNG39ot_E0Th.png"
date: "2020-07-08T03:40:38.787Z"
---

![]({{ site.baseurl }}/images/0uQSfqNG39ot_E0Th.png)

_This week we protested peacefully against the lives wasted coding in lesser languages that don’t rhyme with_ `_poo-basic_` _and argued for a solid hour about the color of a single dot on a page nobody reads. Find out who was wrong about the color of that dot in this week's issue of the Pulitzer Prize winning scholarly publication_ **_The TurtleCoin Weekly Roundup Article, July 7, 2020 Edition._**

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

## node-turtlecoin-p2p

I took a small break from working with the Core suite this past week and circled back to a small Node.js (TypeScript) library I was working up a few months ago. I was able to clean a few things up and put just enough spit and shine on it to feel somewhat comfortable pushing the code up to GH. The end results, is a library that allows you to connect directly to the TurtleCoin® network using Node.js without the need for running a node (ie. the daemon; ie. TurtleCoind). Which may prove very useful for those that want to try their hand at building other things that interact directly with the network. If you’ve toyed with Node.js, feel free to give it a “go” yourself. The library is written in TypeScript but of course it transpiles just fine to CommonJS.

**IBMCD**

[turtlecoin/node-turtlecoin-p2pYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/node-turtlecoin-p2p)

![]({{ site.baseurl }}/images/0LIia3H7qm_rfEhYf.png)

Add your language translation to TurtleCoin.lol and earn your Contributor role in Discord!

## TurtleCoin Website Translations

As you may remember from a previous roundup article, there is a new web designer on the TurtleCoin development team by the name of Daniel_Leedan who is helping us out with a lot of our web based marketing code.

This week, we are working on translations. Daniel_Leedan and TurtleMax collaborated on the Hebrew translation of the web site, and Rock contributed the French translation. Some of these words might not have direct translations, so maybe some of you who might know Hebrew or French can help review the translations we did this week. We would greatly appreciate it if you guys check if your language is already translated by clicking the link below and looking for a file with your country code. If your language isn’t there, copy the `en.yml` file and use it as a template to add your own translations and we are happy to help with the rest! This is a great opportunity to get your pink TurtleCoin Contributor role in Discord :)

Thank you in advance to everyone helping now as well as for the previous round of translations. You guys are great!

**RockSteady**

[turtlecoin/turtlecoin.lolWebsite for TurtleCoin - http://turtlecoin.lol. Contribute to turtlecoin/turtlecoin.lol development by creating an…github.com](https://github.com/turtlecoin/turtlecoin.lol/tree/master/_i18n)

## Karai Updates

What is in a library? This week, I finished up the checklist for phase 1 of the Karai p2p protocol. This is great news because it paved the way for some other things I wanted to do. Lets summarize this week’s progress. This is still my after work and weekend project, so I didn’t hit every objective, but I got a good bit in.

- **Connection process works 100%.** Some of you might remember [this diagram](https://hackmd.io/@ZL2uKk4cThC4TG0z7Wu7sg/H1Ubn6d9L#Node-to-Coordinator-Communication) that IBMCD drew up and I was in charge of building. I got the whole thing wired up and now when a new user joins your channel, your coordinator node walks them through a simple handshake process that ends with an Ed25519 cryptographic access certificate being generated and added to an access control list.
- **Access control works 100%.** As a coordinator you now have a way to limit abusive peers with the ban system. I added a system where you can ban by public key, unban by public key, unban all, and list both the ban list and access list. The commands are documented in the client itself so just hit enter a few times when you fire it up in coordinator mode and you should see a list of the new options. It is an astonishingly simple system that just works by moving certs back and forth from a good folder to a blocked folder. Eventually I will probably build an automated temporary block for abusive peers where if you do not generate a cert immediately after joining 3 times, then your ip or public key gets added to the block list for an hour or so.
- **Extrahash and RockSteady wrote some preliminary libraries** to allow clients written in Javascript and Golang to connect to Karai channels with a few basic commands. Currently the libraries do not support sending transactions, that part is still not implemented far enough in the core client yet and needs to be refactored a bit before libs can support it. Anyway, check out the links below :)

## libkarai-js

![]({{ site.baseurl }}/images/0IFmYIdL-u9FLRrxh.png)

This is Extrahash’s project. It all has to do with this damn dot, you see.. So the library is _technically_ written in Typescript, so Github identified that as Typescript and gave it a blue dot next to the project language designation. Being the guy with a keen eye to design, Daniel_Leedan made a pull request adding the button dot color to each library button on the Karai.io page. Knowing that the libkarai button should be yellow, I went to the github page to find that it was in fact TypeScript, so I changed the label on the button to say TypeScript.

The argument ensued was a waste of time, and I still don’t think we got to the bottom of it, but it looks like I am the only one writing the history of the incident this week, so for the record I am going to say I am right, and you are all wrong, and nah nah nah boo boo.

I will concede the point that Extra made which is that though the tool itself is written in TypeScript, the code it provides or ends up being used in is Javascript, hence the yellow logo I made above. I don’t know why that one is yellow and the dot on the button is blue and says TypeScript, but somehow this works in my mind.

**_RockSteady, Writer of_** **_History, Defender of Truth, Sole Victor, Undefeated, the 3rd_**

## libkarai-go

![]({{ site.baseurl }}/images/0rnUxIsrVHnq2aJOh.png)

libkarai-go being my personal project, as the author of Karai, you would think that this would be the squeaky cleanest example of a reference library that you ever did see..

You would think that, and of course you would be wrong. I will be the first to admit, I did not test this, however when I look at it and visualize it mentally, everything checks out and I am almost positive it compiles. I provide no guarantees that this code will not burn your entire house down.

This could all be just a ruse to Tom Sawyer you guys into doing the tests that I was too lazy to write, or it could be truly terrible code. Time will tell. The graphic looks sick though.

**RockSteady**

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

Join the TurtleCoin pool with the grassiest roots — mine on muxdux.com! [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## Shoutouts & Thanks

_This is the place to mention someone in the community who has done something nice or deserves recognition._

Big shoutout to IBMCD for helping me with the string conversion in the ed25519 library. youre a real lifesaver :D — rock

Thanks to Daniel_Leedan as always for tightening up our web presence! -rock

Thanks to TurtleMax for jumping in to help with the hebrew translation — rock

Welcome to all the new users who joined us this week :) -rock

Shout to the devs, working hard :) — Dreday000

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-7-2020/)_._
