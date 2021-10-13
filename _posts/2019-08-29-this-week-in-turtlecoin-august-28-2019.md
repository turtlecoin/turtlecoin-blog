---
layout: "post"
title: "This Week In TurtleCoin® (August 28, 2019)"
description: "This week, we kicked ass and simultaneously remembered to write about it, further confirming the hypothesis that we live in a simulation. It has been known since TurtleCoin® began picking up steam…"
image: "{{ site.baseurl }}/images/0VLdH0I__wbjwAwt5.png"
date: "2019-08-29T04:44:42.452Z"
---

![]({{ site.baseurl }}/images/0VLdH0I\_\_wbjwAwt5.png)

This week, we kicked ass and simultaneously remembered to write about it, further confirming the hypothesis that we live in a simulation.

![]({{ site.baseurl }}/images/0ys6mW_Tl546Z67B1)

..and even with this, we still can’t get @turtlecoin on twitter.  
Dear @jack, I’m going to need to see some origami.

_It has been known since TurtleCoin® began picking up steam after Bebop lost the bet that something special was happening. The community was coming together in more ways than anyone could have anticipated. People all over the world were flocking to join in the project by creating memes, building tools, contributing code, launching services, hosting public nodes, pools, etc._

_The community has grown quickly and has seen numerous code forks that follow our lead as we aim to provide a place for education, innovation, and hard work that gives rise to a smarter, more involved, and all together better cryptocurrency experience for all. The community was and still is building something special, ney, Turtlely, that we hope will become a household name. Over a year ago, one of us began the process of helping to protect the TurtleCoin® brand that has been built. One of the core began the process of applying for the trademark “TurtleCoin” with the USPTO using their own funds. Today, August 27, 2019, we received word that the TurtleCoin® trademark registration has completed and the registration certificate has been issued. As the USPTO does not issue trademarks to anonymous communities, the core member has assigned the trademark registration to one of their holding companies with the intent to use the mark solely with the TurtleCoin® project._

_Over the course of the next few weeks, you see updates to the project branding guides, website, tools, etc. that reflect the use of the federally registered trademark TurtleCoin®. This is a milestone that many cryptocurrency projects only dream of and often fail to obtain and it is with great pride and excitement that we let everyone know that TurtleCoin® is here to stay._

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

![]({{ site.baseurl }}/images/0BDDALhz0rlN7wI70.png)

[nodes.turtlecoin.lol](http://nodes.turtlecoin.lol/)

**TurtleCoin Blockchain Explorer**

I did a bit of work this past weekend and put together a quick node package that polls the list of Public Nodes from the JSON repository. It keeps track of the history much like <http://trtl.nodes.pub/> but does so on a 2 minute timer instead of a 10 minute one. Then I wired that up to the TurtlePay blockchain cache API ([https://docs.turtlepay.io](https://docs.turtlepay.io/)), added a jazzy display of the data to the Explorer, and hit the commit and push buttons. The result is available via the TurtleCoin Explorer under Nodes. Give it a look and let me know if you have any feedback.

**IBMCD**

[TurtleCoin Block ExplorerBlock Explorer for the TurtleCoin network that is a fun, fast, and easy way to send money to friends and businesses.explorer.turtlecoin.lol](https://explorer.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0CaYjMIjCXpoVzvRe.jpg)

_Zpalmtree (pictured) after the first semi-successful VioletMiner test on ARM boards._

**Violetminer**

“Hello friends,

A week passes so quickly. The ARM optimizations I mentioned last week got completed, but surprisingly, they actually performed worse than the reference implementation! After some investigation, this is actually to be expected. Rotations are quite slow to perform on NEON and this is a large part of the Argon2 algorithm, which might explain the lack of speed. Don’t quote me on that, though. However, the reference CPU still performs pretty well on SBC’s, and for some people may get better performance than xmrig.

As it turns out, GPUs are quite competitive for chukwa, so I have now started working on adding Nvidia support to violetminer. I’ve never used CUDA before, so am not sure how long this will take or if it will be competitive, but hopefully it will turn out well and teach me a lot too.

If this goes well, I’ll also look into adding AMD support — I don’t have an AMD GPU, so would probably have to buy one or rent one of AWS — that’s why I’m starting with Nvidia.

Shoutout to all the guys in the Mining and ARM channels who have helped test or taught me stuff :)”

**Zpalm**

[turtlecoin/violetminerA CPU miner for Argon2i, Argon2d, and Argon2id. Go here to download the latest release. If you prefer to compile…github.com](https://github.com/turtlecoin/violetminer)

**Standalone Web Wallet**

Started working on a client-side web wallet that can be hosted statically (think Github) or ran locally. The interface will allow users to create new wallets which are stored locally on their device. Users can load these locally stored wallets and see incoming and outgoing transactions as well execute transactions, export keys and generate sub-addresses. As default, the wallet will sync against the Blockchain Cache API provided and maintained by TurtlePay, but users will also have the possibility to sync against any daemon of their liking. Currently only generating new wallets work as seen in the video.

**fexra**

![]({{ site.baseurl }}/images/0hSPaNNeSBkaOfM-O.jpg)

**daemon pinger**

This is part 1, part 2 ought to be done next week. All this does is grab the `/info` blob from a TurtleCoin daemon's RPC endpoint and measure how long it took for the request. It has been configured to work with the specifics of Google Functions serverless environment, however, as can be seen, the code can run anywhere that supports Node.js 10\. Will post another update in the next roundup with part 2 :)

**SoreGums**

[SoreGums/daemon-pingerSimple Google Cloud Function to ping TurtleCoin daemons for their /info Once deployed simply POST a JSON blob at the…github.com](https://github.com/SoreGums/daemon-pinger)

## Moving Up!

![]({{ site.baseurl }}/images/03OwzTY135Jfvs9mz.gif)

It’s always good to be recognized! These are the people who gained new roles in the community this week!

- **Fipsi** gained the **TESTER** role this week, thanks Fipsi! Tester role is important to us because it is a self-applied role that people can give themselves if they’d like to be a crash-test-turtle for new releases before they come out. If you’d like to be a Tester, in the discord chat, type `*tester` in any room to get notifications when we have test builds!

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- **Use matches property in ApiDispatcher regex #862**  
  Some calls in the [ApiDispatcher](https://github.com/turtlecoin/turtlecoin/blob/development/src/walletapi/ApiDispatcher.cpp) use a regex, for example, `getTransactionDetails`. They then extract the query parameters. We could instead extract `hashStr` using the `matches` property on the `req` object, by adding a capture group to the hash regex.  
  <https://github.com/turtlecoin/turtlecoin/issues/862>
- **Remove no longer relevant asserts #811**  
  Since pretty much everyone runs the daemon in release mode, instead of debug mode, we’ve ended up where we have a number of asserts which constantly trigger, due to altered/moved/rewritten sections of code.  
  <https://github.com/turtlecoin/turtlecoin/issues/811>
- **Daemon+WalletBackend timestamp adjustments #704**  
  The current /getwalletsyncdata rounds a timestamp to midnight. Depending on what time of the day you start a fresh wallet, you may have no blocks to grab (we need to roll back a bit more than we currently do with the timestamp adjustment), or too many (since it’s rounding to midnight which is quite far away).  
  <https://github.com/turtlecoin/turtlecoin/issues/704>

## Earn TRTL

- **10–20 TRTL** “10 TRTL Bounty — subscribe to DeroGold’s YouTube channel <https://www.youtube.com/channel/UCLKotoL38tq9s87CrapTMzQ> Just ping me and say subscribed and I will take your word for it (will give a total of 20 trtl if you want to post a screenshot confirmation)” **Rogerrobers**
- **500000** “Integrate TurtleCoin in BTCPay Server  
  Info: BTCPay Server is one of the most used, self-hosted, free and fully open-source payment processor project focused on privacy. BTCPay Server has beside other things Point of Sale, Crowdfunding appliations and integration in widely used e-commerce platforms like WooCommerce, Drupal, Presta, Magento. Please don’t take the bounty if you have no intentions to maintain it. More at: <https://btcpayserver.org/> Bonus 100k TRTL if you use TurtlePay™ to get it done” **Elkim**

## Pay With TRTL

In the Discord we have a channel called #Merchandise where people can post things you can buy with TRTL. To view items for sale, check the pinned posts in that channel. These are a few of the items from this week.

All items in our shop:

- **‘Small NEOS Voyager Overshoes’** by **Dustin Thewind | turtleland.fun#1350**ID: #124437
- **‘Alan Wake Collector’s edition (Xbox 360)’** by **Dustin Thewind | turtleland.fun#1350**ID: #196847**'**
- **\-Xbox one games’** by **Dustin Thewind | turtleland.fun#1350**ID: #355973
- **‘Orignal NES in Box’** by **Dustin Thewind | turtleland.fun#1350**ID: #496247**'**
- **Lot of bluray tv series’** by **Dustin Thewind | turtleland.fun#1350**ID: #514474
- **‘eBook’** by **DroppingThePacketsHard²#4751**ID: #726088**'**
- **\-Gigabyte X570 AORUS MASTE’** by **Elkim#7747**ID: #753245**'**
- **\-ASUS X570 STRIX GAMING-F’** by **Elkim#7747**ID: #862191**'**
- **Xbox 360 Slim (120GB) + 9 Games’** by **Dustin Thewind | turtleland.fun#1350**ID: #863214
- **‘Final Fantasy XIII2 Collector’s Edition (PS3)’** by **Dustin Thewind | turtleland.fun#1350**ID: #867107
- **‘Lot of 4 Nintendo Gamecub Games.’** by **Dustin Thewind | turtleland.fun#1350**ID: #957775
- **‘Lot of 5 Game Boy Games’** by **Dustin Thewind | turtleland.fun#1350**ID: #983802
- **‘Lot of bluray movies’** by **Dustin Thewind | turtleland.fun#1350**ID: #994017**'**
- **ASUS X370 ROG CROSSHAIR VI EXTREME’** by **Elkim#7747**ID: #010771
- Provided by fipsi#0789 and DroppingThePacketsHard²#4751

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- Support the only Duck-Themed TurtleCoin Mining Pool <https://trtl.muxdux.com/>

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- **Rogerrobers** Shout out Leo congrats on the baby!!
- **JAPAKAR** DUH di doy doy Thanks to all around here still going strong! I havent been able to get online much at all but looking forward to the 1.8 block!
- **rock** shouts out to all the nerds who made chukwa possible, and all the service providers who made a smooth landing on the latest version good work. thanks to the testers who helped, and thanks to everyone who’s been dedicated to this task of keeping mining fair for as many people as possible. you’re doing good stuff.

![]({{ site.baseurl }}/images/0Xv_MxeBGHgSUmGRN.gif)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-august-28-2019/)_._
