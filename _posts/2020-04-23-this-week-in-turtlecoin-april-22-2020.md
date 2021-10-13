---
layout: "post"
title: "This Week In TurtleCoin (April 22, 2020)"
description: "This week we wrote code with our eyes closed and everything still compiled. Lightsabers are in the mail! This is a place where anybody in our community can submit a post about the TRTL project…"
image: "{{ site.baseurl }}/images/0EEIj1QtTFRnMW6eY.png"
date: "2020-04-23T06:51:08.128Z"
---

![]({{ site.baseurl }}/images/0EEIj1QtTFRnMW6eY.png)

![]({{ site.baseurl }}/images/0Gcw5TO9ljThUV3t5)

**Pictured above**: a Monster Energy Drink molecule

_This week we wrote code with our eyes closed and everything still compiled. Lightsabers are in the mail!_

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

## turtlecoin-wallet-backend

This week I upgraded turtlecoin-wallet-backend to use the 2.0.0 rewrite of turtlecoin-utils. Along with providing a much improved TypeScript interface, this will prep turtlecoin-wallet-backend to be ready for any interaction with Karai, as turtlecoin-utils will provide an easy interface to parse out a Karai pointer from any transaction once we have finalized how we want to store it.

In the process, I also found and fixed a small bug where disabling auto optimization would not work correctly.

**Zpalm**

[turtlecoin/turtlecoin-wallet-backend-jsMaster Build Status NPM Github https://github.com/turtlecoin/turtlecoin-wallet-backend-js Provides an interface to the…github.com](https://github.com/turtlecoin/turtlecoin-wallet-backend-js/tree/development)

## Karai Is Solving The Scalability Problem

For those of you that know the name but don’t quite know what it is, I’ll give you a quick pitch on what the Karai project is, and how it relates to TRTL:

**Background:** Karai started out as one of the early milestones we had with a goal of providing a sidechain to store Ethereum-like smart contracts for the TRTL Network. At the time the approach we were planning to take was all wrong, we were going to launch a single sidechain, with its own currency, using the same linear blockchain software as TRTL with the same inherent drawbacks compounded by the need for extra storage. The headaches were already stacking up and that was not even considering the work that would need to be done to allow people to program their own applications on this thing or be anywhere near up to par with Ethereum, which was a lofty goal at the time.

**Fast forward:** About 2 months ago, as our core software started reaching a point of relative stability we had a moment to step back and look at other initiatives to do some of the much-needed conceptual work we used to do with our free time. As luck would have it, conversations naturally resumed about a new way of implementing Karai that would address some of the concerns we had about our initial approach. Let’s summarize what some of those issues are:

- **A side chain only prolongs the bloat problem** — If spam attacks have taught us anything it’s that if there’s a globally shared asset within easy reach of the masses, someone’s going to put a goatse on it. If you have to sync through the entirety of historic data on-chain from the birth of that particular blockchain just to sync to some data from last month, that’s a problem that gets worse every block whether there is a transaction in them for you or not. Any network with sufficiently fast blocks (like TRTL) and a singular linear chain of blocks will face a problem with scanning and storage eventually.
- **Yet Another Token** **Syndrome** — Karai originally was intended to have its own native coin that was pegged to the value of TRTL to act as ‘gas’ for computation on the Karai sidechain network. The balance between the two plus the third element of relying on merge mined hashrate was a precarious balance and any ability to destabilizing any single element of that would spell disaster. Any sidechain with its own native currency will experience this issue. There is also the issue of token-fatigue which anybody not new to the scene can elaborate on.
- **Linear Blockchains are slow** — Trying to use a linear blockchain for high transaction volume is a nightmare, because the shortest route between A and Z will always be touching every letter between along the way, A, B, C, D, E… Because of this, Bitcoin does less than 4 transactions a second, Ethereum does less than 20 transactions a second, and for comparison, the VISA network claims to do less than 2000 transactions per second..

While we are spelling out a list of our gripes trying to implement smart contracts on a sidechain using conventional means, we might as well address how the new plan solves them.

![https://media.discordapp.net/attachments/453726546868305962/702672129845493790/unknown.png?width=281&height=378](https://miro.medium.com/proxy/0*PGxsfvwN7VBGadLh)

Diagram of Karai’s transaction graph

- **The Sidechain Problem** — Karai transaction channels are numerous and not required to be part of a single sidechain. Another technology using this concept might be familiar to you is Lightning Network technology. In the case of Karai, a new user can connect to 1 channel or many channels, and only has to interact with the history of the swarm they’re connected to. Private and unknown Karai networks are possible by default, the main chain doesn’t have to know.
- **The TurtleCoin vs A 2nd Coin Problem** — Maintaining a secondary asset would fracture the community’s trust and development capacity while also dividing the loyalty and demand between two assets. It’s also a rule of thumb that anything you assign monetary value to will be subject to manipulation and attack with a financial motive. The world does not need yet another token.
- **Linear Blockchains are slow** — Karai is a directed acyclic graph, where there is no single line of blocks to traverse on the path from A to Z. Another network using a directed acyclic graph (or DAG) is IOTA which some of you may know as being particularly fast and unique in the structure in which it arranges blocks. First we should cover that Karai doesn’t have blocks holding the transactions because transactions are independent objects, and it also doesnt have a block interval where empty dust is being produced and recorded for no reason while waiting for transactions.  
  A person connecting for the first time wouldn’t need to pass from A to Z in the transaction history by going through every node A, B, C, D, and so on but instead take only a few hops to scan to the tips of the graph.

With this in mind, last week when I started prototyping some of the code written for the transactional side of Karai, I made a boastful assumption that we could hit a target of _10,000 transactions per second._

I’ll admit that before I was able to write a benchmark or even write a transaction creation method for that many transactions I was already a bit skeptical if I’d just put my foot in my mouth.

Initially when I wrote the benchmark, it was fairly unoptimized, and the way I was creating the transactions and timing the execution of them was a little computationally wasteful, so my first benchmark indicated I was doing 10,000 transactions in a little over 2 seconds. It was disappointing but also inspiring to have a goal to aspire to. It didn’t take long, but with the suggestions of IBMCD and Z, we were able to make some significant improvements in a single night.

![]({{ site.baseurl }}/images/0c-VbLXnLisYGiCn\_.png)

We’ll just come out and say it. **We hit 1 million (1,000,000) transactions** created, processed and recorded to HDD **in under 1 second**. This was with a single threaded benchmark using a Ryzen 1800.

**As a disclaimer**, It’s important to note that in this benchmark we’re not sending any of these transactions over the network, they’re all transactions being created from and processed on the channel coordinator and saved to spinning disk. It’s likely that when we introduce network latency we will incur some slowdown to this number. That being said, these are impressive numbers. Let’s talk about how we derive those numbers.

![https://cdn.discordapp.com/attachments/453726546868305962/701964445378674708/unknown.png](https://miro.medium.com/max/60/0*Pow7dD2zZffRLA9f.png?q=20)

![https://cdn.discordapp.com/attachments/453726546868305962/701964445378674708/unknown.png](https://miro.medium.com/max/860/0*Pow7dD2zZffRLA9f.png)

**The process**, For each of the million transactions, constructed an object consisting of the transaction type, the current hash, the ancestor’s hash, and a JSON object containing the transaction’s own graph position in it. This is a fairly small transaction, but not empty.  
Each transaction generates a separate JSON file on disk containing the Tx data we just covered. The hard drive it was stored on was the same hard drive it was run from, a Western Digital Red 8TB drive. All of this Tx data is then hashed with SHA256 and the process repeats for the next 999,999 transactions.

**Interesting details,** In the process of doing the first benchmark of 10,000 transactions, we noticed that while using the terminal screencapping tool “Asciinema” we were running into the framebuffer becoming our bottleneck with the transaction finishing in 5% of the time it took to render the output to the screen. This was one detail that initially skewed the benchmark readings significantly. Another interesting tidbit we learned is that if you suddenly generate 1 million files into the same folder, two things happen: Git will display a notice that your project can no longer be tracked because it has exceeded the number of files it can watch, and you’ll no longer be able to `rm Tx*.json` the files you just created because the list of files to be fed into the `rm` command will be too big.  
Other things that crashed were my file manager, the game I paused for the benchmark, the YouTube video I was watching, and Winamp.

_I think Winamp just wanted to crash for old time’s sake and should be treated as unrelated._

![https://cdn.discordapp.com/attachments/453726546868305962/702031763970588742/unknown.png](https://miro.medium.com/max/60/0*vNhqEqKD_M2Jf7lE.png?q=20)

![https://cdn.discordapp.com/attachments/453726546868305962/702031763970588742/unknown.png](https://miro.medium.com/max/1400/0*vNhqEqKD_M2Jf7lE.png)

Extras pointer collection service

Also, we figured out how the pointers work from TRTL Network to a Karai transaction channel, and stored a few of them on the TRTL blockchain already, you can check them out on the [official Karai Explorer ](https://karaiexplorer.extrahash.org/)which Extrahash has been making to scan and track all of the Karai channel pointers he can find in the TRTL blockchain and catalog them with some basic data. It’s really cool, you should check it out.

I’m making progress on cleaning up the code base to get it ready to share on Git, it’s written in Go if anybody is looking for something new to learn and want to help out. My current goal is putting the DAG tip selection algorithm into code prototype stage, which shouldn’t be that bad given the speed of current development.

See you next week!

[Karai ExplorerAn explorer for Karai pointerskaraiexplorer.extrahash.org](https://karaiexplorer.extrahash.org/)

Join us in **#Dev_Karai** in the Discord if you have any questions.

**RockSteady (TRTL)**

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**Karai Dev Role** — Extrahash, RockSteady, Zpalm, Ibmcd

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- Madk Shoutouts to mc.evilma.id — the unofficial Minecraft server of turtlecoin.
- greywolf thanks much to zerouan and brätövenhürt for the lively DJ talk show while hosting karaoke
- zerouan thanks yall for supporting vision street wear, lilly meraviglia and not eat any pineapple pizzas
- rock thanks to everyone helping me out with karai, the website, and any of the other irons in the fire we got goin right now

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-22-2020/)_._
