---
layout: "post"
title: "This Week In TurtleCoin (May 20, 2019)"
description: "This week we became car salesmen and tore the blocks up with all the code and project updates, you might want to put a helmet on, we’re going in deep! This week I finished just about all of the Git…"
image: "{{ site.baseurl }}/images/0av9hm_PKtrR-CKGH.gif"
date: "2019-05-21T06:11:07.657Z"
---

![]({{ site.baseurl }}/images/0av9hm_PKtrR-CKGH.gif)

This week we became car salesmen and tore the blocks up with all the code and project updates, you might want to put a helmet on, we’re going in deep!

![]({{ site.baseurl }}/images/04V83cxQUhXYQS4Em.gif)

Pictured: The Developer known as TurtleCoin

## Developer Updates

![]({{ site.baseurl }}/images/0pDnW0sUNRvZwP6Yj.gif)

![]({{ site.baseurl }}/images/0m2ZTRbzLPYQpdRgx.gif)

Git 101 on TurtleEDU

**Git 101 on TurtleEDU**

This week I finished just about all of the Git class for TurtleEDU. This is step 2 of 3 in our mission to turn newbies into knowledgeable users and knowledgeable users into content contributors. After completing the git class you’ll be ready to get your pink Contributor hat in Discord by getting your first pull request merged for something like a wiki article or guide. Git is a very important tool for our work flow and is an essential skill on your way to becoming a developer contributor! Check it out when it’s ready, and in the mean time, take our TurtleCoin 101 class while you wait! Big thanks to sajo for building a git terminal simulator using Xterm JS. **RockSteady**

[TurtleEDUOnline Courses for Blockchain Users and Devs.edu.turtlecoin.lol](https://edu.turtlecoin.lol/)

[https://edu.trtl](https://edu.trtl/) <- visit on the TRTL Network!

![]({{ site.baseurl }}/images/0x-MdDuYf-zbyfASw.png)

Checkpoints on IPFS

**TRTL on IPFS**

Lately we’ve been putting some works on integrating parts of the sync process with IPFS. IPFS allows us to store large files and share them easily, in this case, the checkpoints file was causing github to stop processing them, so while IBMCD worked on getting the checkpoints split automatically, we got them stored on IPFS. **RockSteady**

[TurtleCoin IPFS CheckpointsIPFS: QmYbHVXNJwLQHTptqoj5eX7wQi2hdMfxN6twCSrs1o2QwCns1.turtlecoin.lol](http://ns1.turtlecoin.lol/ipfs)

![]({{ site.baseurl }}/images/061XOwNsPMdRm-qf4.png)

IPFS Gateway

**IPFS Gateway**

If you haven’t heart of IPFS yet, you’ll be hearing more soon. I’ve been working with it a lot lately as a storage network for TRTL, and have already got checkpoints being stored there for use with our daemon.

This here’s an IPFS gateway we’ve built so that you can fetch files from the IPFS network, in this case, you can grab the TurtleCoin Network checkpoints file with ease, all in one file. Use the URL of the gateway as a prefix like you would to download a file through the TRTL Proxy or the IPFS checkpoints. **RockSteady**

![]({{ site.baseurl }}/images/0BOtQpjDNuzXnUEVw.png)

TRTL Proxy

**TRTL Proxy**

You might not have heard, but we have our own .trtl domain service now so you can have a cool domain like fexrasbaby.trtl ( more details at [dns.turtlecoin.lol](http://dns.turtlecoin.lol/)) Most people need a browser plugin to browse the TRTL Network but now you can just put [https://proxy.turtlecoin.lol](https://proxy.turtlecoin.lol/) in front of the url to see what you’re missing without the extra hassle of installing a plugin! **RockSteady**

[TRTL ProxyUse TRTL Proxy to access .trtl TLD websites on the TRTL Networkproxy.turtlecoin.lol](https://proxy.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0iEVAcEYTI7T6BuFy.png)

86 The Roadmap

**Proposal: 86 The Roadmap**

We have so much going on now that there are much better things that deserve to be on the roadmap. The current roadmap is fine, but they’re all distance objectives that require other small incremental changes to come to fruition, so while they’ll still happen it just makes us look immobile.

![]({{ site.baseurl }}/images/02_9tee2OhLX7cPkR.gif)

Hard work goin down round these parts, don’t get none on ya

Originally I proposed that we replace the roadmap with a timeline, with the timeline being a chronological list of launch dates of products we’ve shipped. I don’t think that’s a good idea anymore because it’s hard to say no to well-deserving smaller products that don’t necessarily have the same “visual punch” to their product as other launches. This doesnt mean that they’re insignificant, it means that it would muddy the water when it comes to knocking a first impression out of the park when it comes to what 2 or 3 links a new user clicks. In addition to this tragedy-of-the-commons, we have to be mindful of page load time. Our page is a pretty hefty pageload and I would love to get that down.

So, in the spirit of being the project that doesnt follow in the footsteps of others “come on guys, it’s crypto, you have to have a roadmap and btctalk ann” I say we just get rid of the roadmap and look at doing a “gallery” page that’s an evolution of the ‘timeline’ idea, but abstracted to a page that is off the main index page, but still linked from it. My reasoning for this is that someone who’s interested enough to click our app-gallery link is sufficiently interested to take a minute and click around if we give them a sufficiently fluid browsing experience.

An idea for the timeline is to keep everything purely chronological so that no feelings are hurt, and the most recent project is always ‘features’. This gives incentive to make product launches frequent to keep your name/brand/product at the top of the featured spot.

Let me know what you guys think. **RockSteady**

[86 the roadmap · Issue #144 · turtlecoin/metaWe have so much going on now that there are much better things that deserve to be on the roadmap. The current roadmap…github.com](https://github.com/turtlecoin/meta/issues/144)

![]({{ site.baseurl }}/images/0ktYvEbcj5AABr-KV.gif)

TLD Chatops

**TLD Chatops**

We’re working on a bot that lets a user sign up for a .trtl TLD domain name from dns.turtlecoin.lol in the Discord. So far a lot of people have come to my rescue to make sure I don’t give birth to skynet accidentally.  
Currently the bot validates that you’ve used the correct number of arguments in the command, and the correct type of domain record (thanks IBMCD). Currently the syntax it’s expecting looks like this `.trtl register A mysite.trtl 34.24.25.63`  
Fexra is helping us take it the next mile by adding a few other things to the validation scheme. We hope it will be operational soon and be able to do things like manage recurring annual billing and updating the github records when someone changes a subdomain or adds a new record. **RockSteady**

[turtlecoin/tld-chatopsChatOps bot for .trtl TLD. Contribute to turtlecoin/tld-chatops development by creating an account on GitHub.github.com](https://github.com/turtlecoin/tld-chatops)

![]({{ site.baseurl }}/images/0kYxyEHQa5PL1hYZX.png)

TurtleCoin GitBot

**TurtleCoin GitBot**

A (long) while back, Rock mentioned how cool it’d be if you could make an issue on a github repo without having to sign up or log in; it’d make it a lot easier for new turtles to make bug reports without signing up for another service. I jumped upon the idea and started making the bot. However, it just wasn’t going good; code looked bad, it was long, unefficient and just didn’t work well. I abandoned the project. A few days ago, I starting reading through the docs for the discord.py api (whose rewrite finished and fully launched), and discovered a lot of cool stuff which I had ignored the previous time. Additionally, I had learned a lot in the months between. I started rewriting the bot, focusing on making the code cleaner, look better and making it work more efficiently. So far, I’ve made the basic discord bot, and finished the part which takes in your input for the repository name, and checks if its valid. There’s still a lot left to go, but I’m excited to see the bot finally come to fruition!

Update: The bot is done! I poured some time into it, and finished it a lot faster that I expected! The bot takes in user input for the repo name, issue title, issue body, confirms the detials, then creates the issue and returns the link. It’s currently active and can be called by saying “.git help”. I’m super excited for this, and hopefully you all like it! I haven’t implemented a lot of error handling, so if it ever spits out some error then ping me and let me know. **Sajo8**

[turtlecoin/turtle-git-botContribute to turtlecoin/turtle-git-bot development by creating an account on GitHub.github.com](https://github.com/turtlecoin/turtle-git-bot)

![]({{ site.baseurl }}/images/0RQXaHhdXZwtwt4pr.gif)

CantiLib / CS-TurtleCoin

**CantiLib / CS-TurtleCoin**

Look at me go, I’m actually putting something in the roundup this week! :t_franklin: This week, I put in a bit of time to re-write a lot of the CantiLib / CS-TurtleCoin code that I was never quite happy with. I’ve begun re-writing the P2P back-end, rewrote the entire class that helps serialize and deserialize the packets sent between nodes, and I’ve begun to do further work on deciphering the skynet speech our daemons talk to each other through. Once I hammer out a few more details, I’ll be pushing an update to the dev branch on GitHub. Slow and steady! **Canti**

[turtlecoin/cs-turtlecoinLive repo for TurtleCoin daemon spec and PoC. Contribute to turtlecoin/cs-turtlecoin development by creating an account…github.com](https://github.com/turtlecoin/cs-turtlecoin/)

![]({{ site.baseurl }}/images/0bMpnNyCJtgms_EJc.png)

Wallet sync speed improvements

**Wallet sync speed improvements**

After I mentioned a couple of weeks back, I was investigating rewriting the mobile wallet in C++ for improved sync performance.

I did some more tests and improvements on the C++ code that zedwallet-beta/wallet-api use, and this potential C++ mobile wallet would use.

To begin with, I added block prefetching. Previously, the code would download blocks, process them, and repeat. This causes a delay where we’re waiting for blocks to be downloaded, and not processing anything.

We can alleviate this by using another thread to download blocks constantly, while the main thread processes all the already downloaded blocks. If we can download blocks faster than we can process them, we should see some decent improvements in sync time.

The JavaScript backend already had this, but it was a lot easier to implement, due to JavaScript being single threaded. The C++ code required a lot of thread safe code to be written, which is never fun. Surprisingly, it seemed to work first time! (Fingers crossed).

After some tuning and bugfixes, I did some performance tests, comparing different wallet backends. You can see the results in the first picture. The code changes I made improved the syncing speed from 62 blocks per second, to 312 blocks per second, a roughly 5x improvement!

I have also been doing some work on multi-threading the sync process, but that’s not finished yet, so I’ll leave it for next weeks roundup. **Zpalm**

[WalletBackend block cache + prefetch by zpalmtree · Pull Request #816 · turtlecoin/turtlecoinPrefetches blocks to increase syncing speed. Sync speed comparison: Program Node Type Block Pre Fetch Blocks Per Second…github.com](https://github.com/turtlecoin/turtlecoin/pull/816)

![]({{ site.baseurl }}/images/0S-ghrB8ors_9Uy_2.png)

## Rig Of The Week

![]({{ site.baseurl }}/images/0i94jGWo7HFHoAIa1.png)

[Name: “Lil Crack Hoe”](https://photos.google.com/share/AF1QipPEyzp47JuIE5y0D3JdHlddSDp1uv4bJOhMzHU8UGQP9SAVQmczAht827mFDSs1DA?key=QW5wRlJPTk80XzhlRnNYQXhMTlFzWHI4VG5mV0NR)

I just finished bringing up a RX580 in a Dell 2U 815 Server lol. I’m surprised all this works. I had to hack into the 1100W PDU board in the server and make some power take offs to power the GPU and I had to hacksaw the GPU a little to make it fit, I spent probably 5 hours today trying to get it all together so here is the first test spin!

If your operation exists on an industrial scale, just drive a combine harvester through the field! I spend my day employed as a RF engineering technologist and over the course of 3 years have built a variety of different miners using x86 based architectures running both Linux and Windows mining tools. Over 30,000 (31,000 avg)

## Buy This With TRTL

giving this new section a shot, let us know what you think

![]({{ site.baseurl }}/images/0lVNOaaVFxd-mbUfS.png)

![]({{ site.baseurl }}/images/0GiJfk-kmRgknftTb.png)

![]({{ site.baseurl }}/images/0Euh4j-G3mZZ40i-v.png)

![]({{ site.baseurl }}/images/0yneplBHTto_lf8pE.png)

![]({{ site.baseurl }}/images/08QHnurk_QYJgJW_D.png)

![]({{ site.baseurl }}/images/0CSdYKmgBSHLCYZBE.png)

![]({{ site.baseurl }}/images/0Jwrm3Ooq33qk966T.gif)

Weebles wobble but they don’t fall down. — Iburnmycd

## Turtle Advertising

- CuvéeARM TurtleCoin pool for you! Uptime 2 months, 112 blocks mined, low orphan rate (5.66%), always on and friendly support by @LeoCuvée on the TurtleCoin Discord or via Twitter @CuveeTrtl <https://publicnode.ydns.eu/>
- CuvéeARM TurtleCoin Public Node for sending your large amount transactions. Low power consumption. Powerful. Reliable. Just of you. 1900 TRTL fee per transaction. [http://publicnode.ydns.eu:11898](http://publicnode.ydns.eu:11898/)
- nical but its nice to see comparison, on that page is also links to what I have so far of GPU and CPU rates. :smile: <http://japakar.com/christmaslist/>
- Looking to compare your hashrate to similar cards or processors?! Enter your info here and view others! Thanks so much! <http://turtle.japakar.com/cpu/form.php>
- Mine2Gether’s android mobile miner! Give it a try, make mining with your phone easy! Direct to mine2gether pool. — japakar <https://github.com/Mine2Gether/m2g_android_miner>
- Been tempted to try our TurtleCoin+Loki psolo mining pool, but scared off by the long time to earn a full-block’s reward? Well fear no more!! Activate our PPROP payment scheme and most any miner will see TRTL payouts at least every 1–2 days. And all with NO fees. Cryptonote.Social: where all rewards go to miners. <https://cryptonote.social/trtl>

![]({{ site.baseurl }}/images/0Zy2OtxMiE4D9NC3k.png)

When you hear about “banning bad nodes” be sure to ask what makes a “bad node” vs “bad code”

## Good First Issues

**Remove no longer relevant asserts** ([turtlecoin](https://github.com/turtlecoin)/[**turtlecoin**](https://github.com/turtlecoin/turtlecoin))

Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.

We probably want to remove or update all these asserts to ensure they are still indeed checking things which should be ‘impossible’.

It would also be nice to add more assertions to new code.

I’m not aware how many asserts there are in the current codebase, but it would probably be a good idea to separate this into multiple PR’s for ease of reviewing and testing.

[Remove no longer relevant asserts · Issue #811 · turtlecoin/turtlecoinSince pretty much everyone runs the daemon in release mode, instead of debug mode, we've ended up where we have a…github.com](https://github.com/turtlecoin/turtlecoin/issues/811)

**Add type assertions for JS users** ([turtlecoin](https://github.com/turtlecoin)/[**turtlecoin-wallet-backend-js**](https://github.com/turtlecoin/turtlecoin-wallet-backend-js))

Currently you can pass incorrect types to functions without it throwing. This usually causes hard to diagnose errors. We should add assertions to check each type is as expected, and throw if not.

I think we have lodash as a dependency already, they might help with some of the type checks.

[Add type assertions for JS users · Issue #16 · turtlecoin/turtlecoin-wallet-backend-jsCurrently you can pass incorrect types to functions without it throwing. This usually causes hard to diagnose errors…github.com](https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/16)

## Shoutouts & Thanks

- **greywolf** thanks to all the developers working their asses off in the #dev channels, really behind the scenes to the average user. it’s fun to watch them collaborate on different things in our open atmosphere. well, at least it looks fun to a non-developer. of course, i gotta duck now and then when things start getting thrown around a bit, but it always settles down and is worth the reading.
- **greywolf** thanks to Sierra for always bringing joy and sunshine with her.
- **Japakar** | turtle.japakar.com: dont forget! <http://japakar.com/christmaslist> submit your cpu/gpu hashrate/lower power setting/thread count and whatnot! :smile:
- **Dreday000** Shout out to the TurtleFam !! Just a chill friendly community!
- **Sierra** I wanna just let everyone know I love them and they’re awesome! I pray for yall all the time, sometimes I forget but I’m always thinking of you!
- @**Mrlahaye** “Thanks to @Fexra for buying my PS3 on the #merchandise channel in discord. The TurtleCoin discord is the best place to sell your stuff!!! I’ve been looking to sell this package for months now :) By the way, we’ve got plenty of stuff to sell, please come check it out! <https://discordapp.com/channels/388915017187328002/410839969427357717>
- **RockSteady** Shouts out to SoreGums for the help with the proxy and the cool address tester!
- **RockSteady** proud of bebop this week for getting on his pushups
- **RockSteady** Shoutout to the IPFS & Epona devs for their warm welcome to TRTL, we look forward to building cool things with you and helping the IPFS network
- **RockSteady** Thankful for everyone out there who’s registered a .trtl domain and helped us test out the automation!
- **RockSteady** “Thanks to Thinkpol2 for the help with the DNS automation I was working on, you made it way better than it was.
- **greywolf** thanks to Japakar and anəki for the hashrate collection forms you guys worked on
- **Japakar** is a cool dude! Thanks to Turtle Community for being one of the best! Always fun to be around :)
- **greywolf** i wanna thank Sierra for continuing to be a continuous ray of sunshine in a sometimes dreary environment. muah
- **greywolf** and the realist moniker goes to … zpalmtree
- **Japakar** Thanks so much for the help anəki#0705 !!
- **Japakar** Thanks to Rock and the community! :D Cause you’re awesome. I even punctuated correctly! srs bsns!
- **Frodo** i love turtlecoin ❤
- **greywolf** i wanna thank Japakar for keeping the homeless beggars away from my turtles.
- **Anonymous** What happened to Teacup and the chat history?
- **greywolf** i would like to recognize LeoCuvée’s positive effect on the active community. he’s very helpful in many areas and shares his knowledge in a way that is easily learnable. oh yeah, he’s a polite dude, also.
- **greywolf** (sorry for the overload of shoutouts this week) i am very happy that Sierra is back in the community. she brings a completely different perspective to the group, and she can certainly cause a spark in a sometimes otherwise same-ole-chat-as-usual conversation.

![]({{ site.baseurl }}/images/0V16KvobiA_NFYifJ.gif)

\> When it’s 3AM and people are making meta threads about banning nodes for using the network as intended[.](https://twitter.com/fluffypony/status/1093258621914370050)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-may-20-2019/)_._
