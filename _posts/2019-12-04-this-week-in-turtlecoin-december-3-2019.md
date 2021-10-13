---
layout: "post"
title: "This Week In TurtleCoin (December 3, 2019)"
description: "This week we gained a decent amount of miners from the XMR community. Welcome :) Thank you for helping us grow as a network. This is a place where anybody in our community can submit a post about the…"
image: "{{ site.baseurl }}/images/0VEcFZ7_GifqfXhc3.jpg"
date: "2019-12-04T06:11:51.661Z"
---

![Image result for images of turtles](https://miro.medium.com/max/1400/0*VEcFZ7_GifqfXhc3.jpg)

baby yoda who?

_This week we gained a decent amount of miners from the XMR community. Welcome :) Thank you for helping us grow as a network._

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

## Turtle Wear 2.0

So Turtle wear 1.0 has been around for a couple of years now. One of the biggest annoyances I had when making it was the reliance on a companion app in Android which blocked off iOS and Standalone watch owners from using it. Turtle wear 2.0 is now a standalone application meaning it can be used regardless of your phone and work just fine! It’s also up to date with the latest play store requirements so it’s no longer in danger of being kicked off the app store at the end of the year.

**Seperot**

<https://github.com/turtlecoin/turtle-wear> <https://ijh.dev/>

## Fee per byte

I’ve been working on adding fee per byte to the TurtleCoin codebase. This is where the minimum fee for a transaction is defined by how large in bytes the transaction uses. It makes sense to charge by this metric as the nodes both have to store the transaction and they have to process the transaction, and large transactions are slower to process.

So far I’ve added the code to WalletBackend which drives zedwallet and wallet-api, just need to add it to the daemon and turtle-service. I’ll also need to add it turtlecoin-wallet-backend which drives TonChan and Proton, but that’ll be relatively easy as the codebase is quite similar to WalletBackend.

**zpalm**

[turtlecoin/turtlecoinYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/turtlecoin/compare/development…zpalmtree:fee-per-byte?expand=1)

## Proton v1.1.1 out now!

Hey everybody, there’s a new version of Proton Wallet out now as I’m sure your wallets have already notified you. Check those digits, we’ve made it to v1.1.1! Sick trips!

This is basically a bug fix release. Z and IBMCD were kind enough to find and squash some bugs in the backend that I use for the wallet, as well as some user-reported bugs related to wallet creation and some other things. (Check the changelog if you want the intimate details.)

IBMCD has implemented strict version-checking on his blockchain cache as well, so you’ll find if you do NOT update to the newest walet, your wallet may no longer sync at all. So please update!

Thanks again everybody. As far as what’s next for Proton, I’m planning on beginning work on implementing subwallets (ie, multiple addresses in one wallet file) just as soon as we get deterministic subwallets merged into the backend.

Stay cool TurtleCoin Community,  
**ExtraHash**

[turtlecoin/turtle-wallet-protonYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/turtle-wallet-proton/releases)

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- **Add documentation + examples to all exported functions #67**  
  <https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/67>

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

**greywolf** i can’t thank zpalmtree enough for being the only one with the patience and tolerance to answer the numerous questions from a normie one who is one step away from being tagged with the spoonfed role. i learn slowy, and much of this shit is way over my ability to easily grasp. he is the only one who still exemplifies the qualities of being a good turtle that i read about early last year in an article in Medium that i got linked to from a tweet that was part of a series “What is xxxx”, in which new cryptocurrencies were highlighted every week. that story brought me into the community, and zpalmtree has been very helpful to me all along the painful journey.

**japanesecar** As always, great group! Happy to support it and thank all of you for doing the same!

**anon** applause to the developers and contributors who make this happen

**Zpalm** Congratulations to teacup for winning the Christmas discord logo bounty. If you hover over the discord icon now, it should snow animated snowflakes.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-december-3-2019/)_._
