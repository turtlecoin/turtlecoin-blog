---
layout: "post"
title: "This Week In TurtleCoin (October 16, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0yoghJPK_vHGUMWLM.gif"
date: "2019-10-16T18:48:40.529Z"
---

![]({{ site.baseurl }}/images/0yoghJPK_vHGUMWLM.gif)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

![]({{ site.baseurl }}/images/0SVEgq6rrDsqIhGKa.gif)

TurtleCoin + IPFS

**TurtleCoin Checkpoints**  
People have been using checkpoints for quite some time now to help speed up their daemon in syncing with the network. The generation of the checkpoints has been handled via automatic generation since May 7, 2018\. Since then, like clockwork, and with almost a 100% success rate, the checkpoints have been updated, pushed, and pull requested into the GitHub repository for the entire community to download as needed.

As the chain has grows bigger, the size of the checkpoints file grows as well. GitHub has a maximum single file size limitation without using addons (git-lfs). We worked around the last time we bumped into the limit by separating the checkpoints into two CSV files, the first containing the first million blocks, and the second containing everything else. The two files were joined together into one, compressed, and committed into the repo. Unfortunately, we were quickly approaching the need to split the file again, thereby creating three such CSV files; however, the resulting zip or tarball would have exceeded that same file size limitation. This is a problem for the whole community.

A while back, Rock mentioned something like, “”it would be cool if we could put checkpoints in IPFS””. Such thoughts were noted, tucked away, and you know, forgotten. As I started receiving warnings regarding coming up on the file size limit again, I investigated this option. Over a few days, I’ve put together a new checkpointing service, distribution systems, and leveraged the help of a few IPFS pinning services, to automatically update and deploy the checkpoints into IPFS. The checkpoints latest checkpoints are always available via IPFS and I’ve hijacked the site at [http://checkpoints.turtlecoin.lol](http://checkpoints.turtlecoin.lol/) to provide a list of IPFS gateways where you can pick up the latest checkpoints (timed from your browser), provide details on how to use the checkpoints, given instruction on how to help distribute the checkpoints using IPFS, and even included a few developer tidbits for those of you that want to find the latest checkpoints programmatically.

Enjoy and hit me up in #dev_general if you have any questions or suggestions.  
**IBMCD**  
[http://checkpoints.turtlecoin.lol](http://checkpoints.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0qsuw1-bsOKejI9P6.jpg)

Threaded RPC

**Threaded RPC**  
Been a busy few weeks, in fact I forgot to submit an update last week. The big thing I’ve been working on is putting the daemon RPC server on a separate thread. This allows the daemon to respond much quicker when it’s busy processing blocks and transactions.

The first version was a very simple change, and just passed the existing code through a new server and on a new thread. You can find that here if you want to try it out: <https://github.com/turtlecoin/turtlecoin/pull/903>

This version had a few multi threading issues which could cause crashes or bad data to be returned. So, I’ve been working on a full rewrite of the entire RPC code so I can more easily track down the crashes, modernize the codebase, and more easily add synchronization.

You can find this WIP here: <https://github.com/turtlecoin/turtlecoin/compare/development…zpalmtree:threaded-rpc-wip>

It currently has enough methods added to allow syncing a wallet with zedwallet-beta or wallet-api or proton. Once i’ve re-added all the other methods, I’ll start adding synchronization to fix the crashes with the first version.

Some other benefits of rewriting the whole module include much better CORS support, so you can access the daemon RPC from a browser with more ease, better error messages, and it setting a foundation for being able to build a much more friendly REST api. Finally, it will hopefully make it quicker to add new RPC methods and makes the wallet-api and daemon rpc code very similar.” **Zpalm**

![]({{ site.baseurl }}/images/0Ky5Z8aS6AyjFNxF-.gif)

ExtraHash rollin out after the interview

**ExtraHash Interview**  
Big thanks to ExtraHash for taking time to do an interview with us. For those of you who don’t know, ExtraHash develops our default GUI wallet, and is also our newest Core Contributor, which is quite the accomplishment for someone who started out as a newbie when we initially took him home from the pound! Hope you guys enjoy, and we’d love to hear your suggestions for the next developer to interview for the series.  
**RockSteady**  
<https://blog.turtlecoin.lol/archives/extrahash-interview/>

![]({{ site.baseurl }}/images/0kpZS25oBH0yBvp4D)

TurtleEDU: Intro to Git

**TurtleEDU: Intro to Git**  
The second class for TurtleEDU is ready, this class has Intro to TurtleCoin as a prerequisite, so make sure you’ve taken that first! It covers introductory Git usage which should make you qualified to be a Contributor or Developer if you’re interested in learning.

In this class we create Turtle’s Pizza Shop and use Git to store our pizza recipes in a repository to share with our friends. I think you’ll like it!  
**RockSteady**  
[https://edu.turtlecoin.lol](https://edu.turtlecoin.lol/) <https://edu.turtlecoin.lol/course/intro-to-git>

![Image result for the jeffersons moving on up](https://miro.medium.com/proxy/0*himiGgtM5HtAvrFT)

Congrats to everyone who levelled up this week :D

## Moving Up!

_It’s always good to be recognized! These are the people who gained new roles in the community this week!_

**Footclan** — Iburnmycd

**Developer** — Mufalo

![See the source image](https://miro.medium.com/max/54/0*SzJU38fTZMCqmGc7.jpg?q=20)

![See the source image](https://miro.medium.com/max/908/0*SzJU38fTZMCqmGc7.jpg)

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

- **Cannot scroll up on transfer page #101**  
  <https://github.com/turtlecoin/turtlecoin-mobile-wallet/issues/101>
- **Updated WalletBackend and friends to return daemon rejection message #892**  
  <https://github.com/turtlecoin/turtlecoin/issues/892>
- **Key images are regenerated on transaction creation \[WB\] #842**  
  <https://github.com/turtlecoin/turtlecoin/issues/842>

![]({{ site.baseurl }}/images/07mXNJXWnRWXnEiFL.gif)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

rock — “Such thoughts were noted, tucked away, and you know, forgotten” looool ibmcd

rock — shout out to sisyphus and ibmcd for helping me with the course and quiz content for Intro to Git

Zpalm — Shoutout to fexra for another project started

Japakar is the best in the west of china. — Thanks community and individual members! You all make this place the best!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-october-16-2019/)_._
