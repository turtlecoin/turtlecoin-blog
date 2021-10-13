---
layout: "post"
title: "This Week In TurtleCoin (June 30, 2020)"
description: "This one is a bit of a long read, and some of you might have noticed we skipped last week.. We have big news this week for TurtleCoin, check it out! This is a place where anybody in our community can…"
image: "{{ site.baseurl }}/images/0EEzw2RYqI6voaITW.gif"
date: "2020-07-01T03:55:44.035Z"
---

![]({{ site.baseurl }}/images/0EEzw2RYqI6voaITW.gif)

_This one is a bit of a long read, and some of you might have noticed we skipped last week.. We have big news this week for TurtleCoin, check it out!_

![]({{ site.baseurl }}/images/0wK0Ce0bC5CwtYzqU.gif)

It’s 11PM. Do you know where your Grandma is?

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

## Core Updates

**Boy oh boy were we busy this week.** For those of you following along with the release notes you know that the next release of core is v0.28.0 due out in about a month or so. We’ve committed to make v0.28.0 the last release to include turtle-service. In celebration of moving away from that legacy service, we’ve begun work on the next greatest thing since sliced bread.

![]({{ site.baseurl }}/images/0i7PhzwpUkzBi_R4L.gif)

What could be better than sliced bread you say? **What about a v1.0.0 release of the core software.** Woah… a major version change you say? You’re damn right a major version change. We’re pulling out all the stops with this one. We’re introducing a PoW algorithm change (as Chukwa is quickly coming up on a year old) at block 3M, completely killing off support for turtle-service, and have overhauled the node (daemon) API to get rid of the ugly API calls (json_rpc is dead to us). We’ve replaced the API calls with a REST-like interface that is tons easier for developers to interact with. You’ll also see brand new docs coming out for it (something like <https://meta.turtlecoin.dev/proposals/daemon-api/>) that lays it out beautifully. In addition, we are also introducing a few consensus changes to help everyone keep their sanity.

We will be addressing numerous open issues, increasing performance, and numerous other small changes to improve the core suite. Stay tuned for more updates. Got an idea? Open an issue or hit us up in discord and we will see if it can make the list.

**IBMCD**

![]({{ site.baseurl }}/images/0udq-ICXr7Lmubkp-.gif)

## RocksDB upgrade

This week I got around to cleaning up a ton of warnings and errors that are generated when compiling with a newer compiler, such as clang 10 or GCC 10\. This also included upgrading RocksDB to v6.10.2\. Happy compiling!

**zpalm**

## Coinbase address publishing

In preparation for the v1.0.0 release, I added a requirement for miners to include their public address in the blocks they mine. This helps easily detect network centralization by a single wallet, while still keeping the miner and his transactions anonymous.

**zpalm**

[Require coinbase transactions to prove the destination address by zpalmtree · Pull Request #1073 ·…GitHub is home to over 50 million developers working together to host and review code, manage projects, and build…github.com](https://github.com/turtlecoin/turtlecoin/pull/1073)

[turtlecoin/turtlecoinTurtleCoin is a fun, fast, and easy way to send money to friends and businesses We are a community of people across the…github.com](https://github.com/turtlecoin/turtlecoin)

## Karai Updates

- **We got a new contributor** this week, Hai Turtle who has contributed a few bits here and there after recently learning Go, the language Karai is programmed in. Hai is a long time friend in TRTL land so it was a natural fit. Thanks Hai!
- **We are getting dedicated fields in TurtleCoin** for pointers and notary transactions. Before, we would encode the info and stick it in a payment ID, which just felt dirty for all parties involved. Since Wallet API is changing some, I will be changing the Karai client software to adjust accordingly with our fancy new transaction fields. This sounds like a bunch of fuss over nothing, but I guess a good analogy would be sharing a room with 32 of your siblings and then getting your own room. Terrible analogy but its a roundup, sue me. Nobody reads the Karai udpates anyway :)
- **Progress Updates on connecting to channels:** We can now somewhat connect to channels the proper way. There is a complicated key exchange and signing process that happens over a websocket between the channel coordinator and a joining node. The process we are working on is a means of establishing a cryptographic identity on the channel for the various peers before we go full P2P.
- **Karai integrated with Matrix Chat**: For the last few months or so, I have been using something called Matrix chat, which is like discord or IRC, except anyone can run a server and two or more people can federate their servers together, which spreads out the duty of tracking message history etc. When we arent using Matrix chat to have encrypted chats with the other members of the Illuminati, we are using it to pipe Karai channel messages into the Karai matrix server. This is kinda cool to watch, and currently bounces the data field from transactions in the Zeus staging network into a channel. From day two or so, random people connect sometimes and send test messages, which has been fun to watch.
- **Zeus staging network has been moved to a different host**. Moving to a new host always has its quirks, like in our case where the subtle differences in the server provisioning UI led to me deleting the Zeus staging network twice so far accidentally. That has been lovely, so sorry if that messed up anything any of you were working on. I will be setting up some type of uptime monitor dashboard for Zeus that is hosted on a different provider in case there is an outage at the datacenter level. I have a bad habit of updating the code and then not updating stagenet or updating stagenet and falling asleep before I turn it back on, so a red light green light website thing would be cool.

![]({{ site.baseurl }}/images/0T2TvP5FDe7H1XIaQ.gif)

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles _in the community this week!_

**This week we got two new contributors that have been making waves in our little pond. Big thanks to both of you for your help!**

- **Daniel-Leedan** gets the role of Developer and Karai Developer for submitting code updates to both projects. Over the past week he has added a few finishing touch improvements on our websites, and has been a pleasure to work with. His GIFs are always handy too! Way to go Daniel :)
- Hai Turtle gets the role of Karai Developer for helping me out with some scope issues I was having and for showing me a better way to accept conditional user input. Hai picked up Go fairly quickly and was able to submit a few updates to the Karai core code that really helped us out. Hai is a familiar face in TRTL circles, so it is always a pleasure to have him involved. Big thanks!

![]({{ site.baseurl }}/images/02UNynE85ALjR4apP.gif)

Pictured: A young TurtleCoin contributor on his first day, contemplating his actions in life that led him to this current moment.

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

turtlecoin /violetminer  
**Disable GPU mining on setup** — If a user has a lot of GPUs, but does not want to use them, it would be convenient for them to do this at first run.  
<https://github.com/turtlecoin/violetminer/issues/34>

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

**Create a nice voucher with TipBot.**  
See sample for a link. Real action with Discord TipBot (ID: 474841349968101386)  
<https://redeem.bot.tips/claim/8868ad74-b429-4024-b3e2-6e4037ff83da>

![]({{ site.baseurl }}/images/0zApY6gCenSNEvxWm.gif)

These dollars came from a stripper’s butt. You don’t want that. Use a tipbot voucher.

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- [https://caphillauto.zone](https://caphillauto.zone/) CRITICAL SUPPORT FOR THE CAPITOL HILL AUTONOMOUS ZONE!
- Il Dvce 🐢 I shout @zerouanita that asked me for years my ragù (bolognaise sauce) and when i maked It for him he stopped reply me in DM

![]({{ site.baseurl }}/images/0OzKipG5DpGr6P6t\_.gif)

## TRTL Dev Afterhours

_The afterhours section is a new column we are trying out that aggregates all of the links from #Dev_OffTopic for the week so we can share them with you guys._

<https://www.kernel.org/doc/html/latest/driver-api/fpga/index.html>'  
Submitted by ExtraHash on Sun, 17 May 2020 20:54:59 GMT Lemon Party — A game of bingo gone horribly wrong  
A famous website referenced in popular culture on TV and by celebrities  
[http://lemonparty.org](http://lemonparty.org/)  
Submitted by Crappyrules Ⓤ on Sun, 17 May 2020 20:59:59 GMT The Cyber Security Hub™ posted on LinkedIn  
May 17, 2020: The Cyber Security Hub™ posted on LinkedIn  
<https://www.linkedin.com/posts/the-cyber-security-hub_activity-6667850684374876160-X3xJ>  
Submitted by iburnmycd on Sun, 17 May 2020 21:37:51 GMT Openrouteservice Maps  
Openrouteservice is a open source route planner with plenty of features for car, heavy vehicles, hiking and cycling.  
[https://maps.openrouteservice.org](https://maps.openrouteservice.org/)  
Submitted by RockSteady (TRTL) on Wed, 20 May 2020 13:48:01 GMT The Rogue Experimenters | The New Yorker  
Community labs want to make everything from insulin to prostheses. Will traditional scientists accept their efforts?  
<https://www.newyorker.com/magazine/2020/05/25/the-rogue-experimenters>  
Submitted by RockSteady (TRTL) on Wed, 20 May 2020 15:22:54 GMT Gemini Gateway  
<https://portal.mozz.us/gemini/gemini.circumlunar.space/>  
Submitted by RockSteady (TRTL) on Fri, 22 May 2020 00:57:39 GMT tildeverse  
<https://tildeverse.org/>  
Submitted by RockSteady (TRTL) on Fri, 22 May 2020 05:03:40 GMT GitHub — cris691/discohash: Discohash — A super fast and simple hash. 5GB/s serial (depending on hardware).  
:dancers: Discohash — A super fast and simple hash. 5GB/s serial (depending on hardware). — cris691/discohash  
<https://github.com/cris691/discohash>  
Submitted by RockSteady (TRTL) on Sat, 23 May 2020 16:12:03 GMT GitHub — tevador/hashx: A family of pseudorandomly generated hash functions for proof-of-work and client puzzles  
A family of pseudorandomly generated hash functions for proof-of-work and client puzzles — tevador/hashx  
<https://github.com/tevador/hashx>  
Submitted by cryptonote.social on Sat, 23 May 2020 18:44:45 GMT To merge or not to merge \[part 2\] · Issue #27 · wownero/meta · GitHub  
The last time we had a discussion about merge mining, the general consensus was to push the envelope by adopting RandomJS (RandomX) early in order to serve as an interesting test-bed for Monero. We forked to RandomWOW on 2019–06–14 befor…  
<https://github.com/wownero/meta/issues/27#issuecomment-633108497>  
Submitted by cryptonote.social on Sat, 23 May 2020 18:45:30 GMT ed25519 — The Go Programming Language  
Go is an open source programming language that makes it easy to build simple, reliable, and efficient software.  
<https://golang.org/pkg/crypto/ed25519/>  
Submitted by RockSteady (TRTL) on Sun, 24 May 2020 02:21:21 GMT GitHub — google/tink: Tink is a multi-language, cross-platform, open source library that provides cryptographic APIs that are secure, easy to use correctly, and hard(er) to misuse.  
Tink is a multi-language, cross-platform, open source library that provides cryptographic APIs that are secure, easy to use correctly, and hard(er) to misuse. — google/tink  
<https://github.com/google/tink>  
Submitted by RockSteady (TRTL) on Sun, 24 May 2020 02:38:19 GMT GitHub — k0kubun/pp: Colored pretty printer for Go language  
Colored pretty printer for Go language. Contribute to k0kubun/pp development by creating an account on GitHub.  
<https://github.com/k0kubun/pp>  
Submitted by RockSteady (TRTL) on Sun, 24 May 2020 02:48:38 GMT GitHub — myspaghetti/macos-virtualbox: Push-button installer of macOS Catalina, Mojave, and High Sierra guests in Virtualbox for Windows, Linux, and macOS  
Push-button installer of macOS Catalina, Mojave, and High Sierra guests in Virtualbox for Windows, Linux, and macOS — myspaghetti/macos-virtualbox  
<https://github.com/myspaghetti/macos-virtualbox>  
Submitted by RockSteady (TRTL) on Sun, 24 May 2020 11:44:22 GMT TurtleCoin IPFS Checkpoints  
<http://ns1.turtlecoin.lol/ipfs>  
Submitted by RockSteady (TRTL) on Tue, 26 May 2020 16:49:36 GMT YouTube  
Enjoy the videos and music you love, upload original content, and share it all with friends, family, and the world on YouTube.  
<https://youtu.be/PF3gzLssFzk>  
Submitted by RockSteady (TRTL) on Fri, 29 May 2020 16:24:04 GMT GopherCon 2016: Rob Pike — The Design of the Go Assembler — YouTube

<https://youtu.be/KINIAgRpkDA>  
Submitted by RockSteady (TRTL) on Sun, 31 May 2020 18:29:11 GMT

80-characters-per-line limits should be terminal, says Linux kernel chief Linus Torvalds • The Register  
As he gives us version 5.7 with support for Apple power tech and better exFAT  
<https://www.theregister.com/AMP/2020/06/01/linux_5_7/>  
Submitted by zpalmtree on Mon, 01 Jun 2020 15:33:46 GMT Knex cheatsheet  
One-page guide to Knex: usage, examples, and more. Knex is an SQL query builder for Node.js.This guide targets v0.13.0.  
<https://devhints.io/knex>  
Submitted by zpalmtree on Thu, 04 Jun 2020 21:15:58 GMT LackRack — Eth0Wiki  
<https://wiki.eth0.nl/index.php/LackRack>  
Submitted by ExtraHash on Fri, 05 Jun 2020 17:14:57 GMT Permanent SSH Tunnels with autossh | Linuxaria  
Article by Truelite.it already published on their useful wiki (in Italian) There are many occasions where you need to create connections to machines and services that are protected by firewalls because it is appropriate to adequately protect them, but for which the creation of a VPN becomes an excessive burden. For  
<https://linuxaria.com/howto/permanent-ssh-tunnels-with-autossh>  
Submitted by ExtraHash on Sat, 06 Jun 2020 01:05:37 GMT Welcome — File Browser  
<https://filebrowser.xyz/>  
Submitted by ExtraHash on Sun, 07 Jun 2020 04:48:45 GMT <https://crypto.stanford.edu/craig/craig-thesis.pdf>  
Submitted by if(true) on Mon, 08 Jun 2020 11:37:27 GMT Haiku R1/beta2 has been released! | Haiku Project  
After almost 2 years since R1/beta1, Haiku R1/beta2 has been released. See &ldquo;Release Notes&rdquo; for the release notes, &ldquo;Press contact&quot;, for press inquiries &hellip; and &ldquo;Get Haiku!&rdquo; to skip all that and just download the …  
<https://www.haiku-os.org/news/2020-06-09_haiku_r1_beta2/>  
Submitted by RockSteady (TRTL) on Tue, 09 Jun 2020 22:19:55 GMT

![]({{ site.baseurl }}/images/0gyx9QwgDxqO91hve.gif)

Welp, you made it this far. Have one on us, this week :)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-june-30-2020/)_._
