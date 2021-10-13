---
layout: "post"
title: "This Week In TurtleCoin (August 7th, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0Yo_4Ja-e_tlqyXqT.gif"
date: "2019-08-08T05:05:25.897Z"
---

![]({{ site.baseurl }}/images/0Yo_4Ja-e_tlqyXqT.gif)

![]({{ site.baseurl }}/images/01G0WkmNqoJAjdQTT.gif)

This is it, lads. We made it.

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post, click this link_

![]({{ site.baseurl }}/images/0fC6SSTxyOmj1eB20)

TurtleCoin on an ATM

**TurtleCoin ATM**

GENERAL BYTES, the leading Bitcoin ATM manufacturer from Prague (CZ) and Florida (USA) added TRTL to their range of cryptocurrency ATMs. Operators can now add TurtleCoin to the growing number of ATMs worldwide. We would like to cooperate with the community to make TurtleCoin more accessible to the masses. TRTL is now compatible with all ATMs made since 2013\. Please note that although TurtleCoin is supported on the BATM platform this does not automatically mean that operators will support it on their networks. Ideally someone in the community creates an exchange connection so operators will be able to add TRTL to their network even easier. For now we are excited it works and think it will provide value to the TRTL ecosystem.

**Elkim**

[GENERALBYTESCOM/batm_publicNOTE: Master branch contains new code for an upcoming server release which is not public yet. Please use commit…github.com](https://github.com/GENERALBYTESCOM/batm_public)

![]({{ site.baseurl }}/images/0hXLpgdovimrBVd-6)

violetminer for Chukwa

**violetminer**

The last week I’ve been working on a miner for the upcoming PoW fork, to argon2id / chukwa. This is mainly for fun, I’m not sure if I’ll be able to match the hashrate of other miner developers.

I’ve wanted to create a miner for some time, and this seemed like a good opportunity as there are not that many miners supporting chukwa yet.

So far, I’ve created an argon2 library, which is not yet optimized, but seems to hash at a not too bad rate regardless. I also created a small cross platform sockets library, to help communicate with the pool software. I started building the miner itself yesterday. I’ve only got pool login working with a hard coded username, but hopefully it won’t require much effort to hook up the hashing library, and I can get to work on optimizing it.

I know the current xmrig miner doesn’t work too well on ARM devices, so maybe I can figure out how to get some ARM intrinsics working to squeeze out a little more performance from them. Intrinsics are pretty new to me, so no promises!

Oh — on an unrelated comment, that TonChan update I was talking for a while went out last week. Hopefully it’s working for you all. Sentry flagged up a couple of bugs, but I think they’re pretty minor ones.

**Zpalm**

[https://github.com/turtlecoin/violetminer](https://github.com/zpalmtree/violetminer)

![]({{ site.baseurl }}/images/03iKCq41naPr80WL4)

**turtlerockpaperscissors**

Turtle Rock Paper Scissors is a game boosted with TurtlePay where you can choose between rock paper or scissors to kick the npc machine ass, to start a new game you need to pay the amount of trtl required in the game.  
In case that you survive against the npc machine choice then you will appear in the Half Of Fame where your nickname will be showed to the other players.

Game url: <https://mufalo.online/turtlerockpaperscissors/>

The project is open source and you can get it here: <https://github.com/Mufalo/turtlerockpaperscissors>

**Mufalo**

[Mufalo - OverviewSign up for your own profile on GitHub, the best place to host code, manage projects, and build software alongside 36…github.com](https://github.com/Mufalo)

## Moving Up!

_It’s always good to be recognized! These are the people who gained new roles in the community this week!_

- Congratulations to PstarSR and r00tus3r\_ for earning their pink Contributor roles this week for their contributions to the organization repositories!
- r00tus3r\_ achieved Developer role, earning a bright pink hat for contributions of code to the organization repositories! Great work!

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

- **Use matches property in ApiDispatcher regex**  
  _Some calls in the_ [_ApiDispatcher_](https://github.com/turtlecoin/turtlecoin/blob/development/src/walletapi/ApiDispatcher.cpp) _use a regex, we could instead extract_ `_hashStr_` _using the_ `_matches_` _property on the_ `_req_` _object, by adding a capture group to the hash regex_ <https://github.com/turtlecoin/turtlecoin/issues/862>
- **Remove no longer relevant asserts**  
  _Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code._  
  <https://github.com/turtlecoin/turtlecoin/issues/811>
- **Daemon+WalletBackend timestamp adjustments**  
  _The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away)._  
  <https://github.com/turtlecoin/turtlecoin/issues/704>

## Pay With TRTL

_This is a great place to list items that you’re selling for TRTL_

**FTWJason** in Discord — _Hand made knife_

> This is a Hand Forged low layer Damascus Hunter made from 15n20 & 1084 High carbon steels. 5 piece handle construction. Mokume Gane guard & pommel, diamond shaped brass screw. Dyed Quilted Poplar handle with a stainless steel pin. 5 1/2" blade. 10 3/8" overall. Comes with the leather sheath. Shipped in the United States for 5,310,000 TRTL Internationally shipped for 5,580,000 TRTL This Mokume Gane is a Copper and Nickel silver blend.(edited)

![]({{ site.baseurl }}/images/07fF0-L8bfp37n_dG.jpg)

![]({{ site.baseurl }}/images/0Ltx_dwjBWg1xScwE.jpg)

![]({{ site.baseurl }}/images/0C5YeMxLE61gSCcpx.jpg)

![]({{ site.baseurl }}/images/04k-K-PQLAeOw20H1.jpg)

## Rig Of The Week

![]({{ site.baseurl }}/images/0S5t8BTfeGbiEoCWr)

**“yuge-pp**” by **Turtley McTurtleton McDrizzle**

**“yuge-pp**” by **Turtley McTurtleton McDrizzle**

35 kh/s cn-turtle, 8 kh/s nerva

I’ve been wanting a quad socket setup after doing so many boring sub-$200 dual socket Xeon E5 builds.

I could have saved $100–200 going with a Dell or HP barebones, but noise is a big factor for me. So hashrate per dollar isn’t stellar, but none of my builds are meant to be dedicated miners.

I didn’t have any narrow ILM heatsinks that weren’t 1U, so I borrowed some heatsinks from my other open air setups, modified the unused AMD mounting brackets, and well I guess they’ll do for now. This put me over capacity on that room’s circuit breaker, so those other two machines are turned off now anyway. When I rack it up I’ll grab some Supermicro SNK-P0050AP4.

- Supermicro X9QRI-F+ motherboard
- 4 x Xeon E5–4650 V2 (total 40 cores, 80 threads)
- 16 x 8 GB PC3–12800R (128 GB DDR3 1600 MHz, quad channel)
- Corsair 850w PSU
- Whatever cheap 240 GB SSD Fry’s had on sale until I can get this monster into a rackmount chassis with a proper storage array.

Still waiting on E5–4657L v2 to come down in price so I can swap these CPUs out for some 48 core, 96 thread action.

**Turtley McTurtleton McDrizzle**

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

- Try my turtle node, Germany and West Coast! 5 trtl fee [http://turtle.japakar.com](http://turtle.japakar.com/)

## Shoutouts & Thanks

_This is the place to mention someone in the community who has done something nice or deserves recognition._

- greywolf thanks to Muf for friendship, and being there during difficult times.
- japakar.com TRTL Rocks as always :D Love being around here! Thank you everyone!
- greywolf thanks to CapEtn for working on CHAD TIPBOT.
- rock thanks to zerouan for always keeping us company in the karaoke room :D
- rock thanks to capetn and chadtipbot, i know i give that little bot a hard time but he does a good job
- rock Cheers to all the Developers and Contributors and Service Operators who are still kicking day after day, you’re pillars of the community

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-august-7th-2019/)_._
