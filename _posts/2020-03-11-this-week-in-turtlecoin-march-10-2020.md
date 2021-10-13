---
layout: "post"
title: "This Week In TurtleCoin (March 10, 2020)"
description: "This week we found you can make hand sanitizer for pennies on the dollar by mixing foam peanuts and unleaded gasoline. This is a place where anybody in our community can submit a post about the TRTL…"
image: "{{ site.baseurl }}/images/0b3wAItzEbGIKNVk5.gif"
date: "2020-03-11T05:32:09.620Z"
---

![]({{ site.baseurl }}/images/0RzFJ96dJHZfcXGoz.gif)

_This week we found you can make hand sanitizer for pennies on the dollar by mixing foam peanuts and unleaded gasoline._

## Developer Updates

![]({{ site.baseurl }}/images/0ALNMBFBYyya_0LNb.gif)

TurtleCoin devs booby trapping the links in roundup submissions knowing Pappy Rocksteady has to click them all..  
smdh, yall are playing with the meme master

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post, [click this link](https://www.youtube.com/watch?v=oHg5SJYRHA0)

## LevelDB

Pluton/CapETN recently made a PR adding a LevelDB database backend. This alternative to RocksDB so far is showing some pretty good results in preliminary testing, with faster wallet sync speeds, and reduced database sizes.

This week, I added some extra features to this PR, the main one being allowing swapping database backends at runtime, rather than compile time. This means you can run a LevelDB and RocksDB backed daemon without having to recompile each time. This should help speed up testing of this new database, and if implemented, will allow users to select the backend that works best for them.

![]({{ site.baseurl }}/images/0b3wAItzEbGIKNVk5.gif)

We had some reports that levelDB had high memory usage under Windows when the database was being compacted — I exposed the levelDB max file size configuration as a daemon argument, to test if smaller file sizes causes less RAM usage, as I suspect. Early testing suggests this parameter doesn’t effect database speed, so it may be worth decreasing this for optimal performance.

My changes also improved the database interface to make it easier to implement other database backends in the future. A few months ago, we experimented with lmdb, and Rock suggested BoltDB could be another decent database to try out. This should make it easier for interested parties to try out their favourite database to optimize for their specific daemon usages.

Good work Pluton!

**Zpalm**

[With LevelDB by wrkzdev · Pull Request #1034 · turtlecoin/turtlecoinAdd LevelDB (incl. snappy) during CMake with -DWITH_LEVELDB=true for alternative DB Engine to Daemon. RocksDB is still…github.com](https://github.com/turtlecoin/turtlecoin/pull/1034)

[Allow hot swapping to levelDB at runtime rather than compile time by zpalmtree · Pull Request #1 ·…GitHub is home to over 40 million developers working together to host and review code, manage projects, and build…github.com](https://github.com/wrkzcoin/turtlecoin_rnd/pull/1)

## TurtleCoin RPC Wrapper — Python

“This is going to be the updated TurtleCoin RPC Wrapper in Python for TurtleCoind as well as wallet-api.

The project has already been started by me, and I’m presently working on the wallet-api wrapper which is the new one.

Neither the docs nor the GitHub repo have any content as of now. I’ve the scripts locally and I’m gonna upload as soon as I’m doing alongside making the documentation for the module.

I hope to have it done by the last week of this month. Stay tuned for updates! :-)”

**sohamb03**

[sohamb03/trtl-pyThe TurtleCoin RPC Wrapper for TurtleCoind and WalletAPI. - sohamb03/trtl-pygithub.com](https://github.com/sohamb03/trtl-py)

[Initial pageEdit descriptiontrtl-py.sohamb03.me](https://trtl-py.sohamb03.me/)

![]({{ site.baseurl }}/images/0a_V5MMHzzZK1M4_b.gif)

## CuvéeBits TRTL Mining Pool One Year Anniversary

“Forgotten and covered by some dust sits an ARM board (OrangePI 1+) that I set up as a mining pool about a year to date ago.

We’ve seen good and bad days, at one point the pool (publicnode.ydns.eu) was a top 6 pool, and sometimes it is only a few of my friends using it for almost an equivalent of solo mining.

Some stats for you: Total blocks mined 566, orphan rate about 5.2%, 77 registered addresses, top hash rate about 2.1 MH/s on the previous algo (cn-turtle) and almost 4MH/s at peak times on the chukwa algo.

I run two other pools for TurtleCoin forked projects on ARM boards as well. It proved very reliable, stable, sturdy and powerful enough to accommodate miners of all shapes and sizes, including those with insane hashrate.

Who would expect you can run a mining pool on a credit-card-sized ARM computer that requires little to no maintenance, and that had barely any outage over the past 12 months? “

**Olé Cuvée**

[CuvéeARM Turtle PoolEdit descriptionpublicnode.ydns.eu](https://publicnode.ydns.eu/)

## Hunting for data races in RPC threaded in forked projects

“I spent a good few nights over the past few weeks hunting for core dumps and analyzing them (coredumpctl gdb) across TurtleCoin, DeroGold and WRKZCoin in order to find as many problems with some of the mining pool calls to the daemon via RPC threaded.

As many of you probably know, zpalm did a great job rewriting the RPC daemon code as threaded. The challenge is that now that we unleashed the beast (RPC threaded), it has to interact with the old and ugly dispatcher code, which is single-threaded.

While things look fairly good and stable with TurtleCoin, having help of some of the fork coins proved beneficial — one of the fork coins operate at difficulty target of 20 seconds, and given the network hashrate, miners can mine a lot of blocks — this helped us uncover a few bugs in the blockchaincache code, which in the worst case could badly corrupt database.

As I was discovering the bugs and posted them to our Discord server, zpalm prepared the fixes almost immediately for TurtleCoin, from where myself and I would apply those to with @Pluton to the other two forked coins, testing in production almost immediately :-)

Great to work together with Zpalm and Pluton on this — few more iterations and I believe we will have fixed most of the issues! “

**Olé Cuvée**

![]({{ site.baseurl }}/images/0VkPeBT_DEkfjW2i9.gif)

This is the italian hand gesture for ‘I have to poop, but just a little”

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- **Update user exposed file path opening with error messages #1025**  
  <https://github.com/turtlecoin/turtlecoin/issues/1025>
- **Prevent importing same wallet multiple times #1024**  
  <https://github.com/turtlecoin/turtlecoin/issues/1024>
- **Use matches property in ApiDispatcher regex #862**  
  <https://github.com/turtlecoin/turtlecoin/issues/862>
- **Remove no longer relevant asserts #811**  
  <https://github.com/turtlecoin/turtlecoin/issues/811>

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

![]({{ site.baseurl }}/images/0PkLDEGIHLWkqI7MW)

Weffke’s ‘The Mining Frankenstein’

I’m Weffke, someone who started mining as an experiment, creating this monstrosity. using all 2nd hand parts and learning things the hard way. Currently running 6KH/s with CPU on RandomX on XMR and having the 2 RX550 do a 50KH on trtl

2 RX 550’s (1x 2GB & 1x 4GB), 6GB ECC memory and 2 x Intel(R) Xeon(R) CPU E5–2670 0 @ 2.60GHz cooled by some of the great but ugly Noctua CPU coolers and an old 128 GB SSD.

TeamRedMiner has my back.

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- **PWS TRTL Node \[US West\]** “This is my TurtleCoin node. It’s been public since the last month, and I’ve had a good amount of usage of the node, as evident from the regular fee deposits into my wallet.  
  The node only has a 5 TRTL fee, and I’ve kept it low enough for sustainability on both ends — mine as well as the end users. :)  
  Hoping that y’all will like the node. I’m glad to contribute to the TRTL Community. “ **sohamb03** [http://trtl.sohamb03.me](http://trtl.sohamb03.me/)

![]({{ site.baseurl }}/images/0jImEaQFL_nE4USJO.gif)

- **harrynetwork.uk.to Node** — only 2.5 TRTL transaction fee! I run the currently cheapest (excluding free) nodes so you should use my node to save on the usually more expensive node fees! Try it out now!  
  IP: harrynetwork.uk.to:11898 **Harryw007#3340** <https://explorer.turtlecoin.lol/nodes.html>
- **Small but beautiful** pool in the heart of Europe. Check it out. [https://publicnode.ydns.eu](https://publicnode.ydns.eu/)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- japakar thanks!
- Olé Cuvée Shout out to Greywolf, for dedicating so much time and effort to our projects and for being here! Take a good care of yourself!
- Olé Cuvée Shout out to @Pluton (CapEtn). One of the nicest people I ever met, and a cracking good inspiration for me in things crypto — runs his coin, tipbot across multiple servers and hosts so many other coin nodes (50+ iirc). Hope to meet up in person one day!
- Rock I didnt want to waste space in the main dev roundup area because it seemed too hype-ish, but the conversation about blueprinting the Karai milestone has restarted now that the network is on more stable footing (thanks devs!). If you’d like to know more, or are wondering what Karai is, please check out #dev_karai in the discord and scroll up about a week.
- Rock Thanks to everyone for seemingly being a lot more enthusiastic this week about entering stuff in the roundup :) makes me feel all comfy
- Zerouanita Pepperoni is the best authentic italian pizza only when combined with pineapple, this is true

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-10-2020/)_._
