---
layout: "post"
title: "This Week In TurtleCoin (March 31, 2020)"
description: "This week we jumped on the LISP train so we can all start writing software the way the good lord intended. This is a place where anybody in our community can submit a post about the TRTL project…"
image: "{{ site.baseurl }}/images/08uH-EHgAB84DzYcK.png"
date: "2020-04-01T05:12:31.275Z"
---

![]({{ site.baseurl }}/images/08uH-EHgAB84DzYcK.png)

_This week we jumped on the LISP train so we can all start writing software the way the good lord intended._

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

To submit your post, [click this link](https://youtu.be/6A0p-U1LBbQ?t=5)

![]({{ site.baseurl }}/images/0Qc7vaSvJs2REbqpk.png)

## The New Website

Work is underway to convert the new website from a working concept to an i18n compatible, jekyll-based github static site like our current website on [https://turtlecoin.lol](https://turtlecoin.lol/) .

Earlier this week a volunteer from the chat decided to start the process of porting the new website to markdown. What’s left is turning the various text blobs into mapped quotes for the people who make translations. We try to serve as many regions as possible in their own regional language, so a requirement to launch the new site is for the new site to be i18n ready.

If you’d like to jump in and help out, respond in this issue thread or ping me in the discord and I can get you started.

**RockSteady**

[Port raw html to static github site w/ translation switch · Issue #6 · RocksteadyTC/trtl2020You can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/rocksteadytc/trtl2020/issues/6)

[TurtleCoinTurtleCoin is a decentralized Peer-2-Peer Open Source electronic currency. It's easy to get, completely private, and…rocksteadytc.github.io](https://rocksteadytc.github.io/trtl2020/)

![]({{ site.baseurl }}/images/0Vw7dW9NBKhVg5n5p.png)

**pictured above:** Zpalmtree answering calls on the request line

## wallet-api

This week I added a few new API calls to wallet-api that had been requested by devs.

The first allows you to retrieve all transactions that have a payment ID. This can be useful for people running services where a payment ID is used to identify accounts/users.

The second is along the same lines, but takes a payment ID and returns all transactions with that payment ID. This can allow services to easily retrieve transaction info for a single user.

**Zpalm**

[Add /transactions/paymentid and /transaction/paymentid/{paymentid} endpoints by zpalmtree · Pull…Resolves: #1046github.com](https://github.com/turtlecoin/turtlecoin/pull/1048)

## Wallet-API Lisp

![]({{ site.baseurl }}/images/0QkTXOZ8KkhwOr60F.png)

This project is a wrapper for the Wallet-API wrote in common lisp. It allows the user to implement wallet functions within common lisp.

I hope to further implement this wrapper in other projects with TurtleCoin and continue experimenting with the language. While experimenting I hope to see how well common lisp fits into TurtleCoin and the community at large.

**spfcjic869542**

[turtlecoin/wallet-api-lispWallet-API Wrapper is a wrapper made in common lisp to interface with Turtlecoin's Wallet-API. Quicklisp can be…github.com](https://github.com/turtlecoin/wallet-api-lisp)

![]({{ site.baseurl }}/images/0_bhf7U0_0r5psoBV.gif)

## Karai Transaction Channels

If you’ve been following the conversations in **#dev_karai** over the past month, we’ve been conceptualizing how Karai should work. We’re working on a variation of an idea proposed by Fexra, which at the time was to implement Lightning-Network-like payment channels off-chain that are linked on the TRTL chain by simple pointers to the appropriate Karai transaction channel.

I had some spare time after hours and started working on the design and some experimental code for Karai’s payment channels component. It’s nothing worth pushing to the repos yet but should get there soon.

Currently the software can do a few things:

- add and verify transactions on a local linear chain
- create transactions that hold blobs of data
- print the chain and associated hashes and stored data

It has a list of things it can’t do, but it’s coming together slowly but surely, and it’s a fun personal project to whittle on after work every day to sharpen my Golang skills. Things that took place last week that may have not been mentioned are just little things like assigning a license to the project (we chose MIT license), creating an IPFS peer identity for the Karai node, and some basic TRTL wallet api functions to create/maintain a wallet for paying or receiving pinning fees etc.

None of this is super significant, but I wanted to encourage other devs to move back toward the trend of posting updates for their projects that are in-progress rather than waiting on them being completed before posting. Writing about the process as it happens helps us to show the users that we’re always working hard, and makes them more likely to show up on release day or help out with testing.

**RockSteady**

[RocksteadyTC/go-karaiKarai connection helper written in Go This will launch go-karai git clone https://github.com/rocksteadytc/go-karai…github.com](https://github.com/rocksteadytc/go-karai)

[RocksteadyTC/go-karaiThe go-karai node needs to at a minimum do the following: The go-karai node provides a means for a user to establish…github.com](https://github.com/RocksteadyTC/go-karai/blob/master/docs/DESIGN.md)

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**spfcjic869542** — Developer

**Kinjo** — PR Guerilla

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

**Rock** shout out to to the fellas with the hard hats on in dev_learning putting up with my retardation sometimes :)

> Stop touching your face.
>
> \- Mom

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-31-2020/)_._
