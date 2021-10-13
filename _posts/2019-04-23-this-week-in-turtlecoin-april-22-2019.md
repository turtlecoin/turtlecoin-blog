---
layout: "post"
title: "This Week In TurtleCoin (April 22, 2019)"
description: "This one’s half a roundup and half a feature article, we have some pretty cool stuff to tell you about that we’ve been working on! This is a place where anybody in our community can submit a post…"
image: "{{ site.baseurl }}/images/08cgwEDCCRcouH6Jq.png"
date: "2019-04-23T07:55:24.231Z"
---

![]({{ site.baseurl }}/images/08cgwEDCCRcouH6Jq.png)

_This one’s half a roundup and half a feature article, we have some pretty cool stuff to tell you about that we’ve been working on!_

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your link, click this link_ <https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform>

and now for the part you’ve all been waiting for..

**Let’s pop our beers toast to the big announcement…**

![]({{ site.baseurl }}/images/0lOP2MPPCrUa6Og34)

**.trtl TLD Domain Name System for the TRTL Network**

**We’re doing .trtl domains. Free and paid.**

We’ve set up a cluster of Tier 2 Opennic DNS servers that are currently serving up .trtl domains for the TRTL Network community and associated networks. Right now, that means that you can get your free domain with an A/AAAA record for your fork-project, pool or portfolio, and in the future that means we could be able to do cool things like send funds to someone using regular names instead of a 99 character long wallet address.

Want to skip the nerd talk and check it out? [Click here](https://dns.turtlecoin.lol/)

> Imagine being able to send TRTL to **_wallet.rock.trtl_** instead of  
> _TRTLuxEnfjdF46cBoHhyDtPN32weD9fvL43KX5cx2Ck9iSP4BLNPrJY3xtuFpXtLxiA6LDYojhF7n4SwPNyj9M64iTwJ738vnJk_
>
> Don’t send me any TRTL. I’ll just spend it on Natty Ice and MySpace themes.

Currently the registration process is handled through Github, and there’s a Discord ChatOps bot in the works to handle recurring billing and domain registration duties. Think of this like a .com or a .lol of our own :-)

![]({{ site.baseurl }}/images/0g9d3HFc6sDVzO6Ui.png)

♪♩ Which one of theeeese is not like the otherrrrrrrr ♪♩

To start browsing the .TRTL Network you can start with our port of the Blockchain DNS chrome plugin (Firefox plugin is also done but needs testing) or you can add our DNS server to your network settings at the OS level. Our servers are DNSSEC enabled, and logging disabled, and only delegate .trtl domains so any other requests won’t be blocked or interfered with. You can [check our named and bind9 configs here.](https://github.com/turtlecoin/.trtl)

_Big shout out to the BlockchainDNS project and Opennic for enabling us to build on and improve this system._

**Would you like to help us?** Our browser extensions rely on “API Resolvers” that handle the requests when someone punches in a URL. It’s a simple API for turning DNS requests into JSON responses and has a relatively low resource quota, so if you have some spare servers laying around and want to pitch in, this is a good way to get your Service Operator role!

[If you want to help, say hello in this meta thread.](https://github.com/turtlecoin/meta/issues/142)

You’ll be hearing a lot about TurtleNIC and .trtl here over the next few weeks, and people are already signing up, so be there to get your spot in line before someone snags your next idea for a .trtl domain!

![]({{ site.baseurl }}/images/0Et_Pb0064X-uFVmx.gif)

..and he’s having a hard time holdin these Turtles down! Whoo!

**Wait a second, where does all the money go?**  
Surely we don’t want any handouts, so we have a trick up our sleeve to help spread the wealth a little bit and benefit everyone at the same time..

To put it simply, we’re giving our profits back to the community over a random span of blocks following a premium domain being registered, so that not only can the community have free domains paid for by businesses and larger whale-turtles who want premium domains, but they can be paid a bonus to enjoy this free service and everyone ends up happy in the end.

Added value for miners means more people competing to secure the network, and a few domain registrations are a fine price to pay for that in our opinion, we hope you agree!

You might be wondering, “well if you are giving all of the profits back anyway, why charge anything at all?” The answer is common sense; free things can often become a “Tragedy of the commons” where a small few will sit all day draining resources from the other 95%, squatting domains, draining fountains, and generally ruining it for everyone and returning no value. Our model of sharing the earnings with miners ensures that the profit is returned to the community, and people put thought into what they register by maintaining active web presences.

**_For pricing info, Frequently Asked Questions, and a link to the browser plugins, check out_** [**_dns.turtlecoin.lol_** ](https://dns.turtlecoin.lol/)— rock

![]({{ site.baseurl }}/images/047fRQ5DhdmPL0S_Q.png)

When you’re knee deep in the DNS config and just need to see a ping succeed to restore some faith in your abilities..

**.trtl DNS Chrome Extension**

Rock had this awesome idea for offering up .trtl domains and started building out the infrastructure to support it. Unfortunately, not everyone is as technically inclined as us geeks. Rock found this awesome public domain chrome extension that makes it really easy to support the .trtl domains. As a result, I’ve built out the necessary HTTPS API for resolution, updated the chrome extension code, and published the chrome extension to the google web store. Check it out. **— IBurnMyCD**

[.trtl DNSResolves domains from .trtl name systems as well as all other OpenNIC & other blockchain domain nameschrome.google.com](https://chrome.google.com/webstore/detail/trtl-dns/bmnaipkfomokpndoimalmbfoebbiapch?hl=en-US)

![]({{ site.baseurl }}/images/0wLsU26uV7draKobT.jpg)

Two wild Turtles in their native habitat outside a pub :D

**Z & IBMCD Meetup**

IBurnMyCD and his wife @shelly#4993 crossed the pond last week for vacation and to visit her family for a few days. In their travels around England, the came were well within range of Zpalm Friday & Saturday. Given the opportunity, the group met up in Leeds, UK to put faces with the names over numerous drinks. They hit a few pubs, did wandered the town, and ultimately ended up at what some would describe a “hipster” bar (https://thealchemist.uk.com/) with some tasty drinks.

They’d love to say that lots of geek stuff was discussed but to be fair, they’re pretty much always geek-ing out in discord. Most of their time was spent discussing differences between the USA and UK. They did have a few discussions about a few forks of the codebase (that shall remain nameless), the daemon rewrite, a plausible GUI wallet that isn’t reliant on core code, a little bit about C#, and lots of guessing about the identity of RockSteady. It was fun to finally put a face with the names that they’ve come to know over the last year+.

![]({{ site.baseurl }}/images/0K23qEMHCIhOchJxk)

![]({{ site.baseurl }}/images/0WegK9pKrIITAk5E1)

Before they parted ways, IBMCD handed Z a handful of TurtleCoin coasters (beer mats), window clings, and tent cards to spread around the area. They snapped a quick picture and both parties made their way for their trains. IBMCD was heard screaming, “RockSteady is next” as he went looking for his luggage. **— IBurnMyCD**

![]({{ site.baseurl }}/images/0d0wHQ31-ItQyFt-m.gif)

Happy Bouncing Turtles by Teacup

## Rig Of The Week

**“Rackmount SBC Cluster”**

![]({{ site.baseurl }}/images/07QTXyJExzbsdQQwa)

![]({{ site.baseurl }}/images/0j1F4sCwLBzeqrgiU)

![]({{ site.baseurl }}/images/0U2udKqUoK_Uv-uyH)

![]({{ site.baseurl }}/images/0Cpvu5cmzUffiPY36)

![]({{ site.baseurl }}/images/0WgLp0QBhdb-BloQh)

**Intro**

I am a low-power computing enthusiast and a fan of ARM architecture

**Description**

There are 14 NanoPi Fire3 boards in the front row with 10 OrangePi One+ boards in the second row. Six fans are situated at the front of the rack and blow air past all the boards. The boards use hexagonal standoffs for positioning and are also supported by the ethernet cables on the bottom that feed through the plexiglass.

**Hashrate?**

Approximately 24 kh/s give or take. Each NanoPi Fire3 produces about 1.2kh/s and each OrangePi is producing about 700 h/s. I’m hoping to optimize hashrates more in the future as more stable OS options become available for the OrangePi boards.

**Secrets**

Try to be mindful of power consumption if you can. I mainly view TRTL as a hobby mining project with some good potential upside but I think its important to be mindful of energy consumption nevertheless.

**Notes: This submission came in without an author name unless I missed it. Give me a ping in chat and I’ll put your name up if you see this. — Rock**

![]({{ site.baseurl }}/images/0ZoGH_pz6QozDj5dY)

Submitted by Chiefcoin

## **Bounties!**

**100,000 TRTL —** Adding TRTL support for TrustWallet <https://github.com/TrustWallet/wallet-core/blob/master/docs/Contributing.md#pull-requests> **@SpoofytheWhale**

![]({{ site.baseurl }}/images/03qY9oqn10OEzzm4c.jpg)

![]({{ site.baseurl }}/images/0AbsH68ygpEoT3GL0.jpg)

![]({{ site.baseurl }}/images/0JhrLiECi9iTjuovK.jpg)

![]({{ site.baseurl }}/images/0zdb4SFtcyn9taail.jpg)

Submitted by TenaciousTurtle

## Z’s Good First Issues

Want to give TRTL Development a shot? Feel like getting that hot pink discord role called Developer? We’ve got you covered with another weekly installment of Z’s Good First Issues. These are hand picked gimme-gimme’s for any nerd out there to earn their stripes, you got this!

**Small bug in getFusionTransactionInputs()**

Here — <https://github.com/turtlecoin/turtlecoin/blob/development/src/SubWallets/SubWallets.cpp#L567> we are using `log10` to get the string length of a number. But, `log10(1)` is `0`, not `1`.

We should probably use a method like…

return i > 0 ? (int) log10 ((double) i) + 1 : 1;

(From <https://stackoverflow.com/a/1489928/8737306>)

![]({{ site.baseurl }}/images/0_92P_rU3JadcSHyR)

TurtleCoast submitted by Teacup

## Community Advertisements

- Live in Maryland? Need a 6card open air case? I’ve got one for free. Not shipping cause I just don’t feel like taking it apart. DM Mining4Vets on discord. Need gone asap. Case is one in back with red fans. MINING HARDWARE NOT INCLUDED <https://media.discordapp.net/attachments/548950579632799754/548950923603476481/image0_3.jpg>
- Hands on your hips about extortionate TX fees? [Turtlenode.online](http://turtlenode.online/) strives to provide a reliable and affordable public node service you can trust. You can find it in all reputable GUI wallets; look for the node with a 4.2 TRTL fee and that’ll be [public.turtlenode.online](http://public.turtlenode.online/). The node operator would like to thank everyone for their continued support!

![]({{ site.baseurl }}/images/0vwJKen4AQ9_RaZUh)

Brain Turtle by Morpheus :D

## Shoutouts & Thanks

- **anon** Zpalm is cute :>
- **japakar.com** See you Sierra, you will be missed :) even tho you cant read this!
- **IBurnMyCd** To Z, for only being slightly awkward when we met. I hope you didn’t catch my cold.

![]({{ site.baseurl }}/images/0HlmeO6UbTmuPYVQY.png)

- **greywolf** thanks for rearranging the sequence of the dev channels. now i don’t have to scroll to see if there’s been any new chatter recently in dev general. <https://turtlenode.co/img/dev_general.png>

Big shouts out this week to the Opennic, Blockchain DNS, and TRTL communities for facilitating yet another fun weekend project! -Rock

![]({{ site.baseurl }}/images/0d7FkVtwl0dJKLGLZ.gif)

Sierra would have wanted me to remind you guys to be Good Turtles, brush your teeth and be sure to say your prayers for good hashrate before bed.  
2018–2019  
Sierra T. PalmTree

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-22-2019/)_._
