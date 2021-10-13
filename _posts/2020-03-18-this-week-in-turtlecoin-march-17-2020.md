---
layout: "post"
title: "This Week In TurtleCoin (March 17, 2020)"
description: "This week we stress tested the servers at Netflix from our couch-offices while we tried our best not to breath. This is a place where anybody in our community can submit a post about the TRTL project…"
image: "{{ site.baseurl }}/images/0ZBH130wKHvF6UiPA"
date: "2020-03-18T06:10:59.102Z"
---

This week we stress tested the servers at Netflix from our couch-offices while we tried our best not to breath.

![]({{ site.baseurl }}/images/0NSzy-UMdkrJ78_16.gif)

Buggles was right.

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post, [click this link](https://goo.gl/forms/BNaRYkUmOVOa1apQ2)

## Karai Development

_This is going to be a long one, so,_ **_TL;DR — Karai milestone development started._**

I uploaded a design-doc for the construction of Karai. It covers some of the basic theory for how the side-channels will work, based on an evolution of Fexra’s idea of Lightning-like off-chain channels discussed in dev_karai at the last meeting of the nerds about a week ago.

![https://avatars3.githubusercontent.com/u/39613227?s=200&v=4](https://miro.medium.com/proxy/0*ZBH130wKHvF6UiPA)

> join the convo @ [chat.turtlecoin.lol](http://chat.turtlecoin.lol/)

The jist of it is, we’re using the TRTL chain to store small pointers linking to off-chain ephemeral scripts and content with their own associated transaction channels. These channels carry the history of their user’s interactions with the scripts. The channels are interesting in that they’re made to be hosted by anyone, have transactions instead of blocks, and have a higher capacity for transaction throughput than a normal blockchain. The advantage in the no-blocks-no-chain setup is that if we’re only generating transactions when something actually happens, we can have a very efficient mesh of interconnected transactions in a stream that widens and shrinks according to user volume instead of a single chain of blocks.

Some areas we are still discussing that can use your opinion:

- We have a lot of differing opinions ranging from “do we even need smart contracts” to “should we make our own domain specific language for these scripts” or “should we just let them write scripts in javascript and make the browser do the rendering” and other great ways to get ourselves in deep water. We know the general way in which we’d like to store the scripts and handle content addressing for it, but we’re looking for ideas and opinions regarding parsing and interacting with the stored data. Speaking of stored data, that leads us to the next thing we could use help with..
- Smart contracts aren’t as attractive as they sounded in 2018 for the normal users, and Crypto-Turtles doesn’t sound like a good use for our time, so though we are planning to allow for pinning scripts that can be parsed/interacted-with by Karai, we’re admittedly at a loss for what value this gives the common user at home.  
  The utility of contracts only becomes more evident for businesses, especially so when combined with Multisig which allows, for example a business to create a wallet that requires 3 of the 5 trustees to combine their keys before making a transaction. We’d like to hear ideas from you guys with regards to cool uses for smart-contract-like-things that you like or use on other networks, and it would help us by getting the conversation going in the dev_karai channel so we can cultivate more tangible utility for normal users.

On the development side, currently we have a small list of basic functions outlined in the design doc that I feel we need to reach a suitable mvp. To briefly describe some of the things we have decided on, we are using the libp2p-go library to connect to the IPFS network, which will cover p2p essentials like content addressing, peer management, TLS encryption and NAT traversal for people behind home routers. We also think this is a good idea for p2p because of the fact that this will later allow us to implement caching/pinning of these scripts which should aid in distribution.

Regarding development choices we’ve made, the decision to use Go was because Go has the perks of being a C-like compiled language that can produce a cross platform binary in most cases. Since I’ll be in charge of babysitting and developing this project I wanted it to make sure it is written in something that is a pleasure to read both for others and myself, and is welcoming to new people who may not be as experienced with something like C++.

**RockSteady**

[RocksteadyTC/go-karaiThe go-karai node needs to at a minimum do the following: generate/manage a TRTL wallet (custom prefix?) send TRTL…github.com](https://github.com/RocksteadyTC/go-karai/blob/master/docs/DESIGN.md)

![]({{ site.baseurl }}/images/0I4MUwJtJjWXg8yI\_.gif)

## Blockchain import / export files

This week I have been experimenting with importing and exporting blockchain bootstraps. You can currently import the blockchain from the set of .bin files, but as I think I may have mentioned in another update, I’ve been working on removing those, to save hard drive space to store the blockchain.

Since the .bin files will no longer exist to be imported with, I’ve added a way to export the blockchain via the daemon, and subsequently imported again. It will also support exporting ranges of the blockchain, so you could, for example, import blocks 2 million to 2.2 million, if you want to catch up your daemon which is synced to 2 million and not have to download and import the whole chain.

Another avenue I’m interested in exploring is allowing syncing wallets via importing one of these bootstraps. This should be faster to sync than directly downloading blocks from a remote node, as there will be no database latency and no network latency.”

**Zpalm**

[WIP: No longer require .bin files to be stored by zpalmtree · Pull Request #1033 ·…Needs testing. Needs verification of how corruption is handled. Should save a large amount of disk space. May want to…github.com](https://github.com/turtlecoin/turtlecoin/pull/1033)

> I was bribed paid 999 TRTL to place this ad for a twitch channel here from a guy in the chat. So long suckers, I’m retired now. <https://www.twitch.tv/sythecc>
>
> This was my plan all along. I’m not sorry.  
> \-RockSteady

![]({{ site.baseurl }}/images/0xTcAeCQd24-PKNgl.gif)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-17-2020/)_._
