---
layout: "post"
title: "This Week In TurtleCoin (August 19, 2020)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0LENbKtTY0Zzu3n_E.gif"
date: "2020-08-20T04:43:04.181Z"
---

![]({{ site.baseurl }}/images/0LENbKtTY0Zzu3n_E.gif)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._ [_To submit your post, click this link_](https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform)

![]({{ site.baseurl }}/images/0PWZ_J5MQv27d2NrL.png)

## TurtleCoin Block Explorer v2020

New TurtleCoin block explorer: Beautifully designed, fully responsive and super customizable.

**@l33d4n**

[TurtleCoin Block ExplorerEdit descriptionl33d4n.github.io](https://l33d4n.github.io/trtl-explorer/)

[TurtleCoin Block ExplorerBlock Explorer for the TurtleCoin network that is a fun, fast, and easy way to send money to friends and businesses.explorer.turtlecoin.lol](https://explorer.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0pY6L998CoEL750pi.jpg)

## Boredom Killer #62

Today, for the fun of it, I threw together a quick little easily-deployable P2P, end-to-end encrypted messaging service class, written in TypeScript, which leverages TurtleCoin-Utils + the knowledge I’ve gained from developing TurtleTips. This library lets you encrypt and pass along any arbitrary data string you like between peers — could be used for a chat client, for sharing confidential data between two parties, or passing along any other information you see fit. I may clean it up and release it as a standalone library, or I may hoard it with the rest of my boredom-killing projects, only time will tell. (Insert :t_devilish: emoji.)

**Canti**

![]({{ site.baseurl }}/images/0kZWzhuj5G-ihavDX.gif)

## node-cryptonote-utils

Updated this package for major block 7 coming up at block 3,000,000 and added Typescript types.

I’ve been told that this package is still faster than the block template handling in utils for pool purposes, so challenge accepted.

**IBMCD**

[turtlecoin/node-cryptonote-utilMaster Build Status Development Build Status Note: We build prebuilds of the Node.js native addon module binaries that…github.com](https://github.com/turtlecoin/node-cryptonote-util)

![]({{ site.baseurl }}/images/0fslixaRnfFcRDkOg.gif)

## TurtleCoin-Crypto

Handful up updates published to NPM:

- Updated outdated dependencies
- Separated all interfaces out into their own Typescript file
- The user supplied crypto primitives must now adhere to the ICryptoConfig interface
- Better user cryptographic primitive function handling
- Node.js provided bindings via TypeScript or CommonJS are now async. This is a breaking change for many downstream packages.
- Added support for configurable Chukwa v2 & and other Argon2id variants
- Corrected issue with not including fe_invert.h in \` (thanks @rashedmyt)
- Added support for FreeBSD (thanks @Izder456)
- Switched from TSlint to ESlint  
  Additional tests added” IBMCD <https://github.com/turtlecoin/turtlecoin-crypto>  
  TurtleCoin-utils “Lots of work going on here prepping things for ledger integration. Next release will be published soon.
- Abstract interface defined for LedgerNote And CryotoNote classes (which then makes their use interchangeable)
- LedgerDevice class used to communicate with the app on the Ledger Nano devices
- Incorporated the TurtleCoin-rpc-js package into the library (and kill the stand alone version)
- Pretty much everything moved to async/await (promises)
- Coin configuration abstracted our. Bye, bye config.json
- Added support for the Pool Nonce tag
- Added support for additional tx_extra tags for coinbase transactions
- probably other stuff as well” IBMCD <https://github.com/turtlecoin/turtlecoin-utils>  
  ledger-app-turtlecoin “- Added support for generating a transaction including full signing to the application on device.
- Slightly better memory management
- Few more helper and primitive methods exposed to the host application
- More CI/CD automated testing
- **IBMCD**  
  <https://github.com/turtlecoin/ledger-app-turtlecoin>

![]({{ site.baseurl }}/images/0_jdSomQNjjJ_KWOI.gif)

> **_For the last damn time- turtle-service is dead. Wallet-API is your new daddy._**
>
> Dale Earnhardt Jr.

![]({{ site.baseurl }}/images/0XvBVGp2bBR7SqEit.gif)

## Karai Updates

Recently Karai was wired up to get a steady stream of data flowing into Karai so that some of the data ingest methods and JSON serialization could be tested. To test these methods, Karai learned how to take in COVID19 data, Bitcoin price index data, as well as all of the trade activity of TradeOgre.com. This is pretty cool, and we even got JSON serialization half working, so that is a plus.

The current stagenet, Zeus, is happily chugging along pulling data and stuffing it into transactions that are smoothly being added to the graph.

Next on the horizon are fixing an issue where JSON is being encoded twice causing some forward slash escapes to riddle the nest data objects, and refactoring some of the functions in graph.go to make us a bit more well equipped to begin working on subgraph construction, which as you might remember is what gives karai its weblike appearance instead of a linear chain of transactions.

Also, Daniel_Leedan has been nice enough to start working on a Karai transaction browser template that is based on the design of the new TurtleCoin block explorer, so it should look pretty cool when it is done! I was somewhat pounding my head against the desk while not looking forward to building one so this was a weight off my shoulders. Thanks Daniel_Leedan!

Updates to the Karai website and documentation soon. I get so excited to write code that goes into the Karai core that I sometimes forget to keep the documentation and human side coming, so expect more updates to come!

**Rock**

[KaraiKarai is a universal blockchain scaling solution for distributed applications. - Karaigithub.com](https://github.com/karai)

## New Bounties!

250 A bounty to help with the Turtle 2020 Website translation to pt-br. D4rkGh0st 45000 TRTL We are offering a 45kTRTL bounty for the Russian translation of the website, it is just a few sentences so shouldn’t take much time, a quick win! @TurtleMax

## Good First Issues

_Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!_

![]({{ site.baseurl }}/images/06hp4hML2kid0hCrk.gif)

- **Disable GPU mining on setup #34**  
  <https://github.com/turtlecoin/violetminer/issues/34>  
  If a user has a lot of GPUs, but does not want to use them, it would be convenient for them to do this at first run.
- **Include README.md in releases #19**  
  <https://github.com/turtlecoin/violetminer/issues/19>  
  Just need to update the travis config to copy in the file before zipping/tar-ing

## Free Advertising

_This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup._

Join the Pool With the Grassiest Roots In the Community [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## Shoutouts & Thanks

_This is the place to mention someone in the community who has done something nice or deserves recognition._

Join the Pool With the Grassiest Roots In the Community [https://trtl.muxdux.com](https://trtl.muxdux.com/)

![]({{ site.baseurl }}/images/0Z0BDdDyySRi8B8Mz.gif)

## TRTL Dev Afterhours

_The afterhours section is a new column we are trying out that aggregates all of the links from #Dev_OffTopic for the week so we can share them with you guys._

**MrLahaye** Just wanted to show to you guys my new home office. TRTL theme based.

Godspeed!

**Take part in the Go development research from JetBrains** : golang  
118 votes, 12 comments. Hi Gophers! The JetBrains Market Research & Analytics team is currently holding interviews with Go developers that we would  
<https://www.reddit.com/r/golang/comments/i747w4/take_part_in_the_go_development_research_from/>  
Submitted by RockSteady (TRTL) on Tue, 11 Aug 2020 15:02:46 GMT **TurtleCoin Block Explorer**  
<https://l33d4n.github.io/trtl-explorer/index.html>  
Submitted by l33d4n on Fri, 14 Aug 2020 05:33:31 GMT **Viewing English and Japanese subtitles at the same time**  
<https://richardjharris.github.io/viewing-english-and-japanese-subtitles-at-the-same-time.html>  
Submitted by madk on Fri, 14 Aug 2020 19:02:15 GMT **Wallet RPC documentation | Monero — secure, private, untraceable**
**Monero, a digital currency that is secure, private, and untraceable**  
<https://www.getmonero.org/resources/developer-guides/wallet-rpc.html>  
Submitted by Turtle Max on Fri, 14 Aug 2020 21:45:45 GMT **TurtleCoin Tips**  
<https://turtlecoin.tips/>  
Submitted by zoidbergZA on Sat, 15 Aug 2020 14:47:57 GMT **CoinAPI Documentation**  
<https://coinapi-docs.wrkz.work/>  
Submitted by pluton on Mon, 17 Aug 2020 01:17:06 GMT **Haskell mini-patterns handbook :: Kowainik**  
Kowainik Collection of small Haskell patterns with detailed description, examples and exercises  
<https://kowainik.github.io/posts/haskell-mini-patterns>  
Submitted by RockSteady (TRTL) on Wed, 19 Aug 2020 12:00:55 GMT **Oculus VR will require Facebook login to use devices**  
If existing users don’t want to merge their Oculus and Facebook accounts, they have until January 2023 to use it before support is cut off.  
<https://www.businessinsider.com/oculus-vr-users-log-into-facebook-2020-8>  
Submitted by RockSteady (TRTL) on Wed, 19 Aug 2020 12:25:26 GMT

![]({{ site.baseurl }}/images/0I9vzqi_fjfwtjvFg.gif)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-august-19-2020/)_._
