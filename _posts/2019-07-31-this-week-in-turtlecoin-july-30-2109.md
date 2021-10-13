---
layout: "post"
title: "This Week In TurtleCoin (July 30, 2109)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0qfVNCZAF5wWdt4NT.png"
date: "2019-07-31T05:11:14.005Z"
---

![]({{ site.baseurl }}/images/0qfVNCZAF5wWdt4NT.png)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community. To submit your post, click_ [_this link_](https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform)

> **Congratulations to Lithy (Developer) and Teacup (Contributor) for their new roles this week! :D**

![]({{ site.baseurl }}/images/0yakSxcwa1hRt-Ie6.jpg)

pictured: free-syncing from public nodes in a 2019 soup kitchen

**Public Node**

Sorry I have messed up setting up the server for the node, and I had to start over again with the server droplet. This is the new node IP: [174.138.29.231:11898](http://174.138.29.231:11898/), feel free to connect to it.

**Sabo (Revolutionary)**

![]({{ site.baseurl }}/images/0bH5V797RNxMHCX9Q.png)

Merchandise Bot

**Merchandise Bot**

Hi :) My name is fipsi and I’ve been working on the Merchandise Bot together with @DroppingThePacketsHard2 and @Elkim for the last 2 weeks. The Merchandise Bot can automatically list your items with a title, description and a TRTL price. If you want the bot to auto-update the price of your item, send him a DM with title, description and a fiat price (no market-talk in the Discord). The bot is being hosted by @DroppingThePacketsHard2.  
@Mr. Lahaye discovered an issue with the maximum pinned message count, which limits the amount of pinned messages to 50 per channel..  
So if you have old items in the pinned list (#merchandise) please unpin them and if they’re still relevant, please re-list them using the Merchandise Bot.  
Thank you all for the positive feedback and the great community :t_heart:  
See you in the discord, fipsi :)

**fipsi#0789**

<https://github.com/turtlecoin/turtlecoin-merchandise-bot> <https://github.com/fipsi03/turtlecoin-merchandise-bot>

![]({{ site.baseurl }}/images/0OcD6SqCeYKr7voXy.png)

Nest is back :)

**TurtleCoin’s Nest GUI has been REBORN!**

For all those that have experienced TurtleCoin may have been, or even still, using TurtleCoin’s Nest GUI at one point. After some updates to TurtleCoin’s code, the History section of the GUI seized to work and it was unclear why. A few month’s ago, I posted about forking Nest into a new GUI because I had noticed that every fork of Nest is the exact same but with a different ticker and decimals. So this was my personal mission, to this day I’m still working on it, forking Nest into something new and then IBMCD (IBurnMyCD) had noted to me that the History section didn’t work and I replied that I hadn’t noticed and I will take a look at it. Earlier, whilst syncing my wallet with Nest, I did notice my balance changing but no transactions was getting listed. I did manage to come up with a fix for this, which would fix the whole of the history section. It was funny in a way because I got to build upon my original PR.  
_can you tell I’m proud of this with how much I’m chatting on_  
Anyway, long story short, TurtleCoin’s Nest GUI is fully functional again and it works with TurtleCoin’s latest binaries so you can go back to enjoying Nest again! I will be making more useful PR’s to Nest and _I’ll try and convince Rock to upload my GUI when it’s ready._

**@Lithy / リーチ#9062**

<https://github.com/turtlecoin/turtle-wallet-go> <https://github.com/lithyriolu>

![]({{ site.baseurl }}/images/05sPkI1gbu2sfOhri)

Teacup, and the quest to git gud

**turtlecoin/teacup**

Hey! So I did something I never thought I would do — my first commit on GitHub! I added just about every TurtleCoin image I’ve created so far to the “”teacup”” repository. Feel free to share them or use them any way you like! It’s a sheer pleasure for me coming up with these pictures and I’m inspired to create many more, among other TRTL things…  
Thank you all for such positive feedback. I’m happy to be a part of this with all of you!

**teacup#3556**

[turtlecoin/teacupYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/teacup)

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

**Remove no longer relevant asserts #811**

Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.

We probably want to remove or update all these asserts to ensure they are still indeed checking things which should be ‘impossible’.

It would also be nice to add more assertions to new code.

I’m not aware how many asserts there are in the current codebase, but it would probably be a good idea to separate this into multiple PR’s for ease of reviewing and testing.

[Remove no longer relevant asserts · Issue #811 · turtlecoin/turtlecoinSince pretty much everyone runs the daemon in release mode, instead of debug mode, we've ended up where we have a…github.com](https://github.com/turtlecoin/turtlecoin/issues/811)

**Daemon+WalletBackend timestamp adjustments #704**

The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away).

We should instead just respect the timestamp given, and have a better adjust so we always sync about 100 or so blocks to be safe.

Might require a bit of work, since the timestamp fetching routines I believe hit the two DB caches, which aren’t the most fun to work with.

[Daemon+WalletBackend timestamp adjustments · Issue #704 · turtlecoin/turtlecoinThe current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh…github.com](https://github.com/turtlecoin/turtlecoin/issues/704)

![]({{ site.baseurl }}/images/0IBLUxjoIphd6zO_U.jpg)

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

- Hi, I’m fipsi and if you own a website I need your help :) I need three partners for TurtleAds, an ad service for TurtleCoin. All it takes to be a partner is showing ads on your website using our service. Super simple trust me ;) If you decide to become a partner you’ll be listed on our landing page with your logo, website name and a short description :) Of course you’ll earn from your displayed ads like everyone else will do. DM me if you’re interested and want to learn more: **fipsi#0789**

## Bounty Watch

_Bounties are a great way to earn TRTL for simple tasks!_ _For a quick list of active bounties, visit the #bounties channel and check the pinned posts._

200,000 TRTL **Integrate TurtleCoin in BTCPay Server**  
**Bounty**: Get TurtleCoin integrated in BTCPay Server  
**Info:** BTCPay Server is one of the most used, self-hosted, free and fully open-source payment processor project focused on privacy.  
BTCPay has beside other things **_Point of Sale, Crowfunding_** appliations and integration in widely used e-commerce platforms like **_WooCommerce, Drupal, Presta, Magento_**.  
**Please don’t take the bounty if you have no intentions to maintain it.**  
More at: <https://btcpayserver.org/>

**Contributors:**  
@Elkim#7747–200k

**TOTAL:** 200k TRTL

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- **fipsi#0789** — Thank you @DroppingThePacketsHard2 for hosting the Merchandise Bot and @Elkim for this great project idea. Thanks a lot :t_pirate: ;)
- **rock** — shouts out to lithy and teacup for getting their colors flipped this week :)

![]({{ site.baseurl }}/images/0XvZMHrgfF3kbAZ11.gif)

have a great week :) — rock

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-july-30-2109/)_._
