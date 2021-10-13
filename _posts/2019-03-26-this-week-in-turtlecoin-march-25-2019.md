---
layout: "post"
title: "This Week in TurtleCoin (March 25, 2019)"
description: "Soft Shell Pool Mining — I’ve update the soft-shell algo with a minor tweak to allow for xmr-stak (and other mining software in future) to handle the scratchpad changes at each height, can see this…"
image: "{{ site.baseurl }}/images/0BUUE_WLWrISSgVIg.jpg"
date: "2019-03-26T04:21:08.762Z"
---

![]({{ site.baseurl }}/images/0BUUE_WLWrISSgVIg.jpg)

## Developer Updates

**Soft Shell Pool Mining —** I’ve update the soft-shell algo with a minor tweak to allow for xmr-stak (and other mining software in future) to handle the scratchpad changes at each height, can see this minor tweak here: <https://github.com/turtlecoin/turtlecoin/commit/688087f60dc16b7f6ebfce41287b474cf56f67b5>.  
Trtl-stak has been updated to include the ability to mine Soft-shell and I’ve updated the pool software to send down the required params to the mining software as part of the pool job. **— WhassupZA**

[Add softshell support by davehlong · Pull Request #8 · turtlecoin/trtl-stakrebased to version 2.10 add softshell algo support to minergithub.com](https://github.com/turtlecoin/trtl-stak/pull/8)

![]({{ site.baseurl }}/images/0fzWbGycihzVgrctc)

_image: LeoCuvée_

**TurtleCoin CuvéeARM Pool Update —** “Since the last update, our TurtleCoin CuvéeARM Pool made it out of the shell and does its first baby steps cautiously.  
Blimey, as of today, we’ve got 8 loyal miners (_out of those special thank you Paul, Mira, Vasek and @thinkpol#5064_) — attributing to a pool hash rate of aroud 135kh/s. That’s up from 1 miner (myself) and a decent 35kh/s hashrate from three weeks ago!  
Mind you this all runs on a decent single-board computer (OrangePI One Plus).

We thought we would torture this board with placing all the components to this board — the TurtleCoin node, the Redis db, the turtle-service, the pool software itself and all we would mine would be hot air from orphaned blocks in our cellar-based lab … And no, it’s just running and running (almost 14 days uptime), we’ve mined 32 blocks at the time of writing, no orphaned blocks (yet!) and the board happily idling, waiting for more miners to join! This proves a viable solution. **— @LeoCuvée#1481**

**Mobile wallet —** Not much to report this week. v0.0.6 went out which had a number of bug fixes and enhancements, hopefully that has arrived on your devices by now.  
I think I found the source of some database bugs which were causing crashes, or wallets failing to open, that’ll be coming in the next release.  
If you have an enhancement you’d like to see added to the wallet, please come leave an issue on GitHub :) **— zpalm**

[Transaction address · Issue #53 · turtlecoin/turtlecoin-mobile-walletWould it be possible to add the contact to the details of the transactions on the transaction page? Currently I have to…github.com](https://github.com/turtlecoin/turtlecoin-mobile-wallet/issues/53)

**Cuvée projects in the making (March 2019) —** Times been busy currently at Cuvée. We run number of project for TurtleCoin on ARM-based Single Board Computers (SBCs).

The first project we started almost a year to date ago was a miner based on OrangePI One Plus. Among many other things back then, we’ve heard that TurtleCoin is a CPU-friendly coin, and we just had some boards as left-overs from a commercial project, so we decided to give this adventure a go. A year later and if memory serves us correct two algo changes, we still run a cluster of 12x OrangePI One Plus, 4x OrangePI Zero Plus boards happily mining TurtleCoin at a combined hash rate of 10.5kh/s.

The second project we desperately wanted to make was a TurtleCoin node on the ARM platform. We briefed the TurtleCoin community earlier about the detective approach of hunting down the issue of daemon segfaulting, resulting into a successfull fix by TurtleCoin developers (thanks once again!). Now we run a public TurtleCoin node for syncing wallets (publicnode.ynds.eu:11898). The node runs on the new board called OrangePI 3\. Additionally, we run two private TurtleCoin daemons on two separate OrangePI One Plus boards that serve our Cuvée TurtleCoin mining pool. We run a few other nodes for one of the coins that is a fork of TurtleCoin to support their journey (and opportunity for us to learn and experiment).

The third project we made (and still in the making) is Cuvée TurtleCoin Mining Pool. The mining pool runs again on our favourite board OrangePI One Plus, and si one of our nice surprises. We are really excited how well it runs. If you would like to strengthen us with some of your hash power, the pool runs on ports 3333, 5555 and 7777 again at our (temporary) address publicnode.ydns.eu

The fourth project, with the introduction of the TurtleCoin mobile wallet we started accepting TurtleCoin at our DT Lab & Hub premises in Prague for you to be to pay for coffee and any snacks available onsite when visiting our lab, co-working centre or attending one of workshops that we run.

What else we plan to launch on SBCs related to TurtleCoin?

1. We will be launching server hosting services (Cuvée Physical Private Server — PPS) on ARM SBCs for which you could pay with TurtleCoin. Lots of building and testing currently ongoing. Soon we will be launching social network channels to share our journey with you.
2. We will be offering ready-made plug & forget TurtleCoin products:  
   a\] your own private plug & forget TurtleCoin node with pre-synced blockchain against which you can synchronize your wallet, in slick black alu enclosure that contains the Rock64 SBC from Pine64 project.  
   b\] your own private mining pool pre-configured  
   c\] clustered-miner based on OrangePI One Plus SBCs (cluster of 3, 5 and 10 miners)
3. All we do we will share with the TurtleCoin community on Discord and on our social media channels, as well as all code & images that we develop as part of our projects will be avaiable for everyone on GitHub.

Our long-term plan? We want to put together a TurtleCoin POS solution. Initial planning, looking for suitable components and drafting already started. Long way ahead though.  
Stay tuned for regular Cuvée TurtleCoin project updates :-) **@LeoCuvée**

**BountyBot** — A project to better organize and list all available bounties. This will be a multi-server bot capable of handling a complete line of settings, custom command prefixes, and custom subdomain for showing a searchable index of bounties for your server. Current progress holds at 72% of desired features.

Special thanks to @fipsi | The Machine#0789 for the original base of the BountyBot.

This bot is being created in response to the Bounty listed by @anəki#0705 and @DiscoTim#3647 GitHub Source Coming soon” **— TwixtedTurtle (@TwixtedChaox#9638)**

[TwistedStudiosLLC/BountyBotA project to better organize and list all available bounties on a discord server. - TwistedStudiosLLC/BountyBotwww.github.com](https://www.github.com/TwistedStudiosLLC/BountyBot)

## Rig of the Week

![Japakar's rig "Turtley" ROTW](https://miro.medium.com/max/34/0*1xotuAfWWxHxZk61.jpg?q=20)

![Japakar's rig "Turtley" ROTW](https://miro.medium.com/max/1152/0*1xotuAfWWxHxZk61.jpg)

![]({{ site.baseurl }}/images/0VsuKM1HzQuoCZ6YO.jpg)

**Japakar’s rig, “Turtley”**  
**Details:** Its simple and small, but it works! Bronze 750watt power supply, xfx rx 570 8 gig, 8 gigs of ram  
**Hashrate:** 5.5 kH/s (CN_Turtle)  
**Secret mining tips?** Keeping the hands out of the pants and above the table.

## Bounties

1000 TRTL — I need windows and mac binaries for my fork of turtlecoin please. @Monster(QPSA)

## Community Advertising

Always find the cheapest node for your wallet! <https://notrait.com/>

On the go and need to sync your TurtleCoin wallet or make a transaction? Use our relieable, trusted and cutting-edge CuvéeARMTrtl public node at publicnode.ydns.eu:11898\. It runs on OrangePI 3 hardware and only charges 19 TRTL per transaction.

After a few days of me not realizing, I am updated! Nodes 1 and 2 are back and working 100%! Sorry about that! turtle.japakar.com and turtle2.japakar.com [http://turtle.japakar.com](http://turtle.japakar.com/)

Another paper wallet generator! It cant hurt to have too many of a good thing! [http://turtlewallet.japakar.com](http://turtlewallet.japakar.com/)

2 turtle nodes for your turtle pleasure! turtle.japakar.com and turtle2.japakar.com Thanks for using them! [http://turtle.japakar.com](http://turtle.japakar.com/)

## Shoutouts & Thanks

anon Zpalm is cute :>

greywolf thanks a bunch to the guys (always) talking in dev_general. i visit several times daily just to follow the different discussions. there is always something to learn.

greywolf thank you for the generous gift to my TonChan wallet, the turtle who sent this transaction: hash=e3fe4338309724c1e7e0b7e6724abc1530954159648218f6040a42efe060bb97

LeoCuvée #1481 Massive thank you to @zpalmtree for all his work on the Ton Chan mobile wallet. A big step forward for TurtleCoin in my humble personal view. Thank you!

@leocuvée Shout out to @Rogerrobers for this one — resonates with me :) <https://media.discordapp.net/attachments/471023390954618883/557346992427368460/unknown.png>

SoreGums nice one Blyadman coming along and posting a PR for russian translation out of nowhere for the client side web wallet turtlecoin/turtlecoin-webwallet-js

japakar.com | turtle.japakar.com derogold.japakar.com toomuch.japakar.com Thanks to my fellow turtles! This place still rocks. Get it? Thanks for being there, for coming up with new ideas and for being the coolest group on Discord. Looking forward to another year.

anon shout out to alium you are no longer welcome in the lad compound

not rock — its okay alium they dont like me either

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-25-2019/)_._
