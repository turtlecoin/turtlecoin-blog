---
layout: "post"
title: "This Week In TurtleCoin (May 13, 2020)"
description: "This week we got a lot of new community members, as well as a lot of returning faces, which is always a treat! Some of you even contributed translations for the new website. Welcome to all of you…"
image: "{{ site.baseurl }}/images/0RA4eTn1AuThwdtUh.gif"
date: "2020-05-14T04:16:20.414Z"
---

![]({{ site.baseurl }}/images/0RA4eTn1AuThwdtUh.gif)

This week we got a lot of new community members, as well as a lot of returning faces, which is always a treat! Some of you even contributed translations for the new website.

**Welcome to all of you just joining us and those returning, we hope you tell a friend :)**

[**https://chat.turtlecoin.lol**](https://chat.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0m3KW3VLTxBXQjtgt.gif)

Pictured above: Fexra returning from a busy shift at the TurtleWallet datacenter. Fun fact, this is also where the Myspace servers are kept to this day.

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

## Bobberino and the struggles with github builds

![]({{ site.baseurl }}/images/0zO60ZmWJrBt1nOQX)

Only while typing in this caption box do I realize how badly I messed up the alignment on old Bob there.

How do I say this delicately… While we are very thankful for Github for providing this free service, we’ve reached some quirky limitations of the service across a few projects. To sum it up, Github Actions has about a 1 in 6 chance of just outright refusing your trivial non-breaking changes and not building an otherwise fine Golang project.

This exact issue happened to me in fact and I got frustrated, I’ll admit. All I wanted was some cross platform binaries for Windows, Mac, and Linux. That’s all I wanted, nobody gets hurt..

I guess in a fit of impatience I realized it doesnt have to be that hard, and discovering the command to list all of the different OS’s and architectures I could compile for just on my own, the path forward to easy cross platform binaries became clear.

Bobberino is a tool that for legal reasons I couldn’t call ‘Bob The Builder’, so I gave him a different name with similar role. If you want to use it, you install Bobberino, then call him up inside of any Go project and he’ll generate your binaries and zip them up in a folder inside of \` ./builds/<os>/<cpu>\` for anything from Android to Windows to Plan9 and OpenBSD. Bobberino even builds his own binaries!

I know there’s probably 2 people out there who use Golang, and you probably have a much cooler solution so by all means ping me about what would make it a good tool for you so that we can share it with more than just those who wish to compile Karai. Thanks :)

For the rest of you, enjoy all the sweeeeet sweeet binaries to choose from :)

**Rock**

[karai/bobberino👷 Bobberino is a simple cross-compiler tool for Go projects - karai/bobberinogithub.com](https://github.com/karai/bobberino)

## TurtlePay Blockchain Cache

About a week ago, Extra and I struck a deal that if I altered the blockchain cache started returning rawblocks for syncing, that he’d volunteer 2 hours a week for 8 weeks at a nursing home to get to know some random elders and learn from them (after the COVID-19 stuff passes).

Keeping up with my side of the bargain, I’ve been exploring different ways to store the blockchain data in a traditional database again. This includes restructuring the database schema, playing with different database systems, and thinking about where I can push some of the load off the API and database itself and push some of the heavy lifting elsewhere.

To get ready for some of that, I’ve laid the foundation by putting together a database abstraction layer that ultimately allows for swapping the backend database for the cache using a variety of different database systems. Right now, I’ve baked in support for MySQL/MariaDB, Postgres (and any of it’s derivatives), CockroachDB, Yugabyte, SQLite, and may tackle a few others.

My expectation is that that by refactoring, rewriting, and redefining the schema, I’ll be able to upgrade the cache software to make it better, faster, stronger, and more resilient. I believe I’ll also be able to make it a lot easier to scale the software and, at least for my deployment of it (the TurtlePay copy), deploy it in a more geographically friendly way that brings a lot of the data closer to the masses. These changes, among others, will help the cache respond a lot faster to everyone overall.

**IBMCD**

![]({{ site.baseurl }}/images/0IwcD2kuDLeNP3XTm)

## Aardvark TurtleCoin Node

Aardvark is a public node running on bare metal with 32GB RAM, dedicated SSD storage, and RGB lighting which looks really nice at night. You can use it to sync your wallet and make anonymous transactions on the TurtleCoin network. **19morpheus80** **on GitHub**

[Mining PoolEdit descriptionsync.tippyturtle.com](http://sync.tippyturtle.com/)

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

![Related image](https://miro.medium.com/proxy/0*ftDUTYkzg3FDq8bt)

Above: The workers at Herominers busy not-spreading the hashrate.

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

> “For the record I’ve been using Aardvark TurtleCoin Node for 35 years and it’s never let me down. “
>
> Rusty Turtleford , Senior Citizen

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

anon — Shouts out to the lads who died in the struggle

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-may-13-2020/)_._
