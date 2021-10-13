---
layout: "post"
title: "This Week In TurtleCoin (September 16, 2020)"
description: "As some of you who follow the dev pipeline may already know, we nerds on the TRTL core team have been busily working on bringing TurtleCoin into being a legitimate version 1.0.0 product. We are so…"
image: "{{ site.baseurl }}/images/07_bGOrzLvtNOtmWa.gif"
date: "2020-09-17T05:10:41.346Z"
---

![]({{ site.baseurl }}/images/07_bGOrzLvtNOtmWa.gif)

Wew it sure has been a while since the last update hasn’t it?

Big Karai updates in this issue :)

# Developer Updates

## TurtleCoin 1.0 Is Ready!

_As some of you who follow the dev pipeline may already know, we nerds on the TRTL core team have been busily working on bringing TurtleCoin into being a legitimate version 1.0.0 product. We are so excited to say that this goal has been a success!_

To those of you outside of programming circles, what this means is that over time, through many planned efforts, we have rewritten and improved enough of the codebase that we are no longer the same TurtleCoin software that was initially released years ago.

This change is significant because we are doing away with a lot of legacy technology in favor of newer interfaces that make TRTL an easier network integration for commercial or professional use cases. Turtle Services is going away in favor of the newer Wallet API, so exchanges and web wallets will have newer integrations that are already in the pipeline and ready to try today, and also the daemon has lots of much needed improvements. In the old days of TRTL a daemon outright crashing in the middle of the day several times was normal, and we used to write software to manage those quirks- now it is almost unheard of that a daemon or wallet crashes without extreme circumstances.

What 1.0.0 means to you is **more value from TurtleCoin** as a product when you recommend it to people, and more technical potential for serious services to adopt our network for their products. These improvements to the software as a whole make us better equipped as a developer team to help them with their integrations and engineering questions. **If you operate a service such as an exchange or e-commerce website that wants to integrate with TRTL, send your developers to us so we can answer their questions and help make it a pleasant transition.**

**Users**: You still have time to upgrade, and as always, your TRTL isn’t going anywhere if you don’t upgrade, you will just need to update before you want to access them next time. As always, don’t forget to export your keys or seed phrase for safekeeping, and download the newest release when it becomes available from [latest.turtlecoin.lol](http://latest.turtlecoin.lol/)

_Big thanks to IBMCD and Z who have put a considerable amount of time into core, and all of the helpers along the way who helped us get where we are today!_

**Rock**

[Release v0.28.3 · turtlecoin/turtlecoinMaster Build Status Upgrade to this release is highly recommended and upgrade to any 0.28.x release is mandatory for…latest.turtlecoin.lol](http://latest.turtlecoin.lol/)

![https://user-images.githubusercontent.com/8020386/91375139-71a4b680-e84c-11ea-8503-7f3774678224.png](https://miro.medium.com/max/60/0*H7yid3q7chH3cb_l.png?q=20)

![https://user-images.githubusercontent.com/8020386/91375139-71a4b680-e84c-11ea-8503-7f3774678224.png](https://miro.medium.com/max/1400/0*H7yid3q7chH3cb_l.png)

**TurtleCoin® Open Issues Browser**

## **TurtleCoin® Open Issues Browser**

Keep track of all the open issues in one place.

**@l33d4n**

Code: <https://github.com/turtlecoin/trtl-issues>

Demo: <https://turtlecoin.github.io/trtl-issues/>

![]({{ site.baseurl }}/images/0i8tgL29vpCzFJXMp)

## Karai Questions

_A few questions come across quite a bit, and I always wish there were some sort of link I could toss into the chat as a diversion as I run away. Today we will fix that. Here are some common questions that I dont always have time to type out an eloquent answer for:_

- **Q:** **What is Karai?**  
  **A:** _Karai is a high volume network-agnostic off-chain scalability and communication layer for disparate networks._  
  **Longer Answer:**  
  **Karai is high volume** because when tuned correctly it can process over a million transactions per second.  
  **Karai is network-agnostic** because although TRTL is natively baked in, Karai can be integrated with any other network such as ETH, BTC, XMR, etc.  
  **Karai is an off-chain scalability and communication layer** in the same way that you would use Lightning Networks to bring more capacity for tracking events offchain on the BTC network, Karai can be used in a similar way to reduce overhead and fees by offloading event volume onto an off chain network without an extra token or cost. By this same concept, Karai can signal events on **one or many networks simultaneously**, which opens the door for possibilities like atomic transfers and other activities that transcend individual network borders.
- **What is Karai a fork of?** Karai is written 100% from scratch, and is not a port or effigy of any other networks or products. Karai is written in Go on nights and weekends by one person under the critical stare of others.
- **What problem does Karai address?** BTC and other networks that require fees for transactions and have a finite burst capacity for traffic, for example when CryptoKitties came around, ETH clogged up fast. Karai addresses this by moving traffic off the main network onto ephemeral side networks that can notarize their state on their main network for a fraction of the cost of operating all on chain.
- **What about smart contracts?** Smart contracts require a perfectly tuned and executed programming environment inside of a box with tools we provide that may well shoot your eye out if you don’t build them just right, and often require _yet another token_ to work. Karai doesn’t need another token, and it doesn’t force your code into a box full of holes.
- **Can Karai do ${BUZZWORD}?** No.

# Karai Tech Updates

_There are almost too many things to update you guys on, so lets hit some short bullet points of the \*recent\* things that have gone into the pipeline:_

- **Vultr** evicted us from their platform, so be sure to give them a middle finger and 0 dollars for the trouble they have caused the next time you see them.
- **Two new stagenets** have been added to replace the one that Vultr destroyed. You can now use the two networks to test your Karai applications. As always, uptime for both networks is listed on our uptime page at [uptime.karai.io](http://uptime.karai.io/) provided by the good folks at [UptimeRobot.com](https://uptimerobot.com/)
- **Icarus**, or the unstable stagenet, is where the bleeding edge breaking changes happen. Code from the private Karai git gets deployed here. Currently this stagenet is operating fully dockerized with a DB backend that interfaces with Elastic Search, Postgres, Sqlite, MySQL, and others.
- **Daedalus**, or the stable stagenet, is operating with in-memory data structures for holding its transactions. Daedalus has much less volume, but has a higher capacity of transactions per second, as it is 100% based in RAM, writing raw JSON to disk as needed for preventative measures.
- **Subgraphs are live** on Icarus. Daedalus is still running in blockchain mode. What this means is that Karai has gone from operating like a blockchain to being a full [directed acyclic graph](https://en.wikipedia.org/wiki/Directed_acyclic_graph) similar to IOTA, Nano, and other DAG networks. When visualized, the transactions are no longer single file objects all in a straight line. Graphing a Karai network history ends up looking like a fractal of endless trees and branches. (see the picture above) This sounds like a bunch of magic but has been the biggest step forward by far for Karai.
- **Karai explorer** is a new product from the hands of Daniel Leedan and ZoidbergZA. The explorer will be a way for users of Karai to check out the transactions flowing through their networks, and to help them examine the data in each tx if they desire. To give the most TRTL like experience possible, I have added a `/stats` endpoint to the Karai API that gives useful data about the network and coordinator, along with a `/transactions` and `/transactions/txhash` endpoint to give access to the full graph history as well as a specific lookup per transaction by tx hash similar to the way we do on TRTL now.
- **New interfaces** Currently if you have a desktop or mobile application that you are writing, you can integrate with Karai using our Go and Javascript/Typescript libraries. The downside is if your app is written in something else besides Go and Javascript, like C# or Crystal, you would have to write your own connections by examining the Karai coordinator code yourself. We have had a few offers to port the libs to other languages when the overall API stabilizes, but as with most things we will be making plants to write our own libs if the need is there.  
  **What languages would you like a Karai lib for? Do you have the skills to implement the APIs in your language of choice? Drop a line in #dev_karai and let us know what you want to see.**
- **Docker and Makefiles** have brought some much needed streamlining to the dev process. If you have docker installed, you can launch a few containers and have Karai up in no time with just a few commands from our handy dandy makefiles. When I am launching Karai to test a development build I just type `make karai` and I am off to the races. Pretty cool for very little extra work.
- **Transaction metadata**, as I have stated before, is the next step development-wise after subgraph construction. Subgraph construction is in a comfy state of done-ness. It works, however it is un-optimized, but still ready for use, so the next goal would be to add the metadata to the different parts of a subgraph.
- **Let us review the parts of a graph real quick to get an idea of why we need metadata:**
- The first transaction in a Karai graph is the root tx. Think of this like a genesis block, in TRTL terms. Karai has a strict definition for this transaction, a type 0 transaction, which only appears once in any graph.
- Immediately following the root tx is a metadata-only transaction called a Milestone. Its job is to set rules for how the subgraphs connected to it are constructed, like how sudden bursts of millions of transactions should be handled, as well as handling user data like public addresses of participating nodes that own transactions in a subgraph following a milestone. This allows for faster scan speed over traditional blockchains that must scan the entire chain from root to tip to find their own records.
- Each milestone has subgraphs as child graphs from that point. Each subgraph has a designated subgraph leader. The leader is determined by using the first transaction in a subgraph and appending an extra metadata field to it that contains data relevant to transactions in the rest of the subgraph. If your public key doesnt appear in that subgraph leader, you can skip syncing that subgraph if it doesnt mean anything to you.
- Subgraphs are created by starting a timer when the first transaction is created, and keeping a creation window open to gather transactions flowing in during the interval. When the timer finishes, the subgraph is closed and assembled in its final formation, and the metadata is written to the subgraph leader’s header data.

_I think that is a good summary of the important parts, but as always I am leaving out a lot of context, details, and design decisions you might want to know more about._ **_If you want to know more, direct yourself to the dev_karai room in the Discord._**

**Rock**

[KaraiKarai is a universal blockchain scaling solution for distributed applications. - Karaigithub.com](https://github.com/karai)

[Karai Stagenet Uptime MonitorEdit descriptionuptime.karai.io](https://uptime.karai.io/)

![]({{ site.baseurl }}/images/02lZZP51ccd7q366G.jpg)

Hey officer guys! Check out these really cool embroidered patches that Akupara made! They cost **only 1M TRTL**, which at todays prices are a steal of a price. Get yours today!  
**CONTACT AKUPARA IN DISCORD FOR MORE INFO**

## Meme Artistry

_I saw a bunch of memes in the Discord by the user TUᴙTlɘᴙAiᴎ and immediately said that they must go into the roundup. I dont have a name for this column so Im just going to call it what it is, pure artistic skill. Big thanks to TUᴙTlɘᴙAiᴎ for these contributions!_

![]({{ site.baseurl }}/images/0MjW_9ojcWCHJC6Yw.gif)

![]({{ site.baseurl }}/images/0ETcSZ0_I6Q6njYiD.gif)

![]({{ site.baseurl }}/images/0dJCw0LEYdEopImiF.gif)

![]({{ site.baseurl }}/images/0OvlmrghVf1I6Jcve.gif)

![]({{ site.baseurl }}/images/0QjvHD_PWLBVakJ2O.gif)

![]({{ site.baseurl }}/images/0A71nKrYrq_FkKs9N.gif)

![]({{ site.baseurl }}/images/0BPFej3mSYxT7fcrH.gif)

## Off Topic But Still Cool

![]({{ site.baseurl }}/images/0WH4p4iIsoB-A9F5x.png)

This is something one of our TRTL devs made that is not necessarily TRTL related but still pretty damn cool! Check it out! It is a game programmed in the style of old Game Boy games <https://skizot.itch.io/skydrop>  
**Good job Skizot :)**

## Good First Issues

_I used to pester the same person every week for these, but now we have a nifty explorer to check them out,_ [_look at it here!_](https://turtlecoin.github.io/trtl-issues/) _Thanks Daniel Leedan! Good First Issues are a good starting point for any beginner developer who wants to jump in and help out._

**turtlecoin/turtlecoin-wallet-backend-js**

- [**More prepared transactions functions**](https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/83)
- [**Add documentation + examples to all exported functions**](https://github.com/turtlecoin/turtlecoin-wallet-backend-js/issues/67)

**turtlecoin/turtlecoin-mobile-wallet**

- [**Add transaction filtering**](https://github.com/turtlecoin/turtlecoin-mobile-wallet/issues/4)

**turtlecoin/violetminer**

- [Disable GPU mining on setup](https://github.com/turtlecoin/violetminer/issues/34)
- [Fail compilation when using nvidia and unsupported host compiler](https://github.com/turtlecoin/violetminer/issues/29)
- [Cache CUDA download](https://github.com/turtlecoin/violetminer/issues/24)

## Free Advertising

_Free advertising for any TRTL related services and service providers!_

Join the Pool With the Grassiest Roots In the Community [https://trtl.muxdux.com](https://trtl.muxdux.com/)

## TRTL Dev After Dark

_This is a collection of the links that are pasted into dev_offtopic that we collect with a bot that ExtraHash wrote. Thanks!_

DiceKeys | Crowd Supply  
Security keys you create by rolling dice  
<https://www.crowdsupply.com/dicekeys/dicekeys>  
Submitted by iburnmycd on Sat, 22 Aug 2020 13:51:17 GMT @adlrocha — Network Coding in P2P Networks — @adlrocha Weekly Newsletter  
Linear combinations on-the-fly!  
<https://adlrocha.substack.com/p/adlrocha-network-coding-in-p2p-networks>  
Submitted by RockSteady (TRTL) on Mon, 24 Aug 2020 04:30:52 GMT GitHub — jmoiron/sqlx: general purpose extensions to golang’s database/sql  
general purpose extensions to golang’s database/sql — jmoiron/sqlx  
<https://github.com/jmoiron/sqlx>  
Submitted by RockSteady (TRTL) on Tue, 25 Aug 2020 02:17:01 GMT There You Go Wow GIF by Kontrast Werk — Find & Share on GIPHY  
Discover & share this Kontrast Werk GIF with everyone you know. GIPHY is how you search, share, discover, and create GIFs.  
<https://giphy.com/gifs/kontrast-werk-mindblown-lfaig-nh1-iD6CVE4PrSqhhHdyYR>  
Submitted by RockSteady (TRTL) on Tue, 25 Aug 2020 15:08:35 GMT Arwes — Sci-Fi UI Framework  
Futuristic Sci-Fi and Cyberpunk Graphical User Interface Framework for Web Apps  
<https://arwes.dev/>  
Submitted by RockSteady (TRTL) on Wed, 26 Aug 2020 15:09:18 GMT TurtleCoin Open Issues  
<https://l33d4n.github.io/trtl-issues/>  
Submitted by l33d4n on Thu, 27 Aug 2020 02:04:42 GMT <https://github.com/turtlecoin/trtl-issues/invitations>  
Submitted by RockSteady (TRTL) on Thu, 27 Aug 2020 02:08:06 GMT trtl-issues/repos.json at master l33d4n/trtl-issues GitHub  
TurtleCoin Open Issues Browser v2020\. Contribute to l33d4n/trtl-issues development by creating an account on GitHub.  
Https://github.com/l33d4n/trtl-issues/blob/master/repos.json  
Submitted by l33d4n on Thu, 27 Aug 2020 02:10:20 GMT <https://github.com/turtlecoin/trtl-issues/invitations>  
Submitted by l33d4n on Thu, 27 Aug 2020 02:12:43 GMT GitHub — turtlecoin/trtl-issues: TurtleCoin Open Issues Browser v2020  
TurtleCoin Open Issues Browser v2020\. Contribute to turtlecoin/trtl-issues development by creating an account on GitHub.  
<https://github.com/turtlecoin/trtl-issues.git>  
Submitted by zpalmtree on Thu, 27 Aug 2020 02:14:17 GMT Repositories — GitHub Docs  
<https://docs.github.com/en/rest/reference/repos#list-organization-repositories>  
Submitted by zpalmtree on Thu, 27 Aug 2020 02:16:49 GMT <https://api.github.com/orgs/turtlecoin/repos?sort=updated>\`  
Submitted by zpalmtree on Thu, 27 Aug 2020 02:17:04 GMT Repositories — GitHub Docs  
<https://docs.github.com/en/rest/reference/repos#list-organization-repositories>  
Submitted by l33d4n on Thu, 27 Aug 2020 02:20:06 GMT trtl-issues/main.js at master l33d4n/trtl-issues GitHub  
TurtleCoin Open Issues Browser v2020\. Contribute to l33d4n/trtl-issues development by creating an account on GitHub.  
<https://github.com/l33d4n/trtl-issues/blob/master/dist/js/main.js#L102>  
Submitted by zpalmtree on Thu, 27 Aug 2020 02:22:51 GMT <https://media.discordapp.net/attachments/579918539830460417/662493503271731238/image1.gif>  
Submitted by zpalmtree on Thu, 27 Aug 2020 02:23:10 GMT GitHub — turtlecoin/trtl-issues: TurtleCoin Open Issues Browser v2020  
TurtleCoin Open Issues Browser v2020\. Contribute to turtlecoin/trtl-issues development by creating an account on GitHub.  
<https://github.com/turtlecoin/trtl-issues>  
Submitted by RockSteady (TRTL) on Thu, 27 Aug 2020 02:25:35 GMT Speed up loading with parallel api requests by zpalmtree Pull Request #1 turtlecoin/trtl-issues GitHub  
Issues:

Spacing on issue labels and number of issues is broken. It seems like there was extra whitespace in the original version. Probably best fixed with some margins.  
Scroll bar seems to not work

Note: I removed the spinner. It doesn’t seem needed when the page renders and starts loading issues near instantly.  
<https://github.com/turtlecoin/trtl-issues/pull/1>  
Submitted by l33d4n on Thu, 27 Aug 2020 05:09:59 GMT

<https://api.github.com/orgs/turtlecoin/repos?sort=updated>',  
Submitted by zpalmtree on Thu, 27 Aug 2020 05:14:41 GMT <https://raw.githubusercontent.com/turtlecoin/trtl-issues/master/repos.json>\`  
Submitted by zpalmtree on Fri, 28 Aug 2020 00:43:01 GMT Back To The Future Biff Tanner GIF — Find & Share on GIPHY  
Discover & share this Biff Tanner GIF with everyone you know. GIPHY is how you search, share, discover, and create GIFs.  
<https://giphy.com/gifs/reaction-65DcceNYwMBs1nGATv>  
Submitted by RockSteady (TRTL) on Fri, 28 Aug 2020 01:13:47 GMT Will Smith IDid It GIF — WillSmith IDidIt Happy — Discover & Share GIFs  
The perfect WillSmith IDidIt Happy Animated GIF for your conversation. Discover and Share the best GIFs on Tenor.  
https://tenor.com/view/will-smith-i-did-it-happy-excited-omg-gif-8068878  
Submitted by l33d4n on Fri, 28 Aug 2020 01:15:05 GMT <https://turtlecoin.github.io/trtl-issues/>  
Submitted by l33d4n on Fri, 28 Aug 2020 01:21:25 GMT TurtleCoin Open Issues  
<https://turtlecoin.github.io/trtl-issues/>  
Submitted by l33d4n on Fri, 28 Aug 2020 01:31:30 GMT Make loading ordered by zpalmtree Pull Request #2 turtlecoin/trtl-issues GitHub  
Slightly slows down initial paint  
<https://github.com/turtlecoin/trtl-issues/pull/2>  
Submitted by zpalmtree on Fri, 28 Aug 2020 01:34:15 GMT How to Install Android OS to Run Favourite Games and Applications in Linux  
Android is a project which aims to port the Android system to Intel x86 processors to let users install it easily on Linux, Windows systems, or using Virtualbox.  
<https://www.tecmint.com/install-android-in-linux/>  
Submitted by iburnmycd on Fri, 28 Aug 2020 13:11:24 GMT The A.R.M. Terminal — a Cyberdeck for your desk BACK7.CO  
My concept for this project has been pretty clear since the original idea. I love the movie The Matrix, and I often wonder about many movies like it if they had included 3D printing or other newer tech in their universe. I loved the look and idea of a floating terminal, and many of us already have  
<https://back7.co/home/arm-terminal>  
Submitted by RockSteady (TRTL) on Fri, 28 Aug 2020 14:13:22 GMT GitHub — turtlecoin/trtl-issues: TurtleCoin Open Issues Browser v2020  
TurtleCoin Open Issues Browser v2020\. Contribute to turtlecoin/trtl-issues development by creating an account on GitHub.  
<https://github.com/turtlecoin/trtl-issues>  
Submitted by RockSteady (TRTL) on Sun, 30 Aug 2020 00:23:12 GMT Breast Cancer Love GIF by Mighty Oak — Find & Share on GIPHY  
Discover & share this Mighty Oak GIF with everyone you know. GIPHY is how you search, share, discover, and create GIFs.  
<https://giphy.com/gifs/love-halloween-pink-l378p60yRSCeVoyAM>  
Submitted by RockSteady (TRTL) on Sun, 30 Aug 2020 01:25:07 GMT Aluminum Monitor Stand USB 3.0 Hub ports with fast charge Metal Riser Support Transfer Data and Charging,Keyboard|Laptop Stand| — AliExpress  
Cheap Laptop Stand, Buy Quality Automobiles & Motorcycles Directly from China Suppliers:Aluminum Monitor Stand USB 3.0 Hub ports with fast charge Metal Riser Support Transfer Data and Charging,Keyboard  
Enjoy Free Shipping Worldwide! Limited Time SaleEasy Return.  
<https://www.aliexpress.com/item/4000744985776.html>  
Submitted by l33d4n on Wed, 02 Sep 2020 08:06:28 GMT <https://www.amazon.com/Charging-Station-Organizer-Compatible-Smartphones/dp/B07ZNDQYKS>  
Submitted by iburnmycd on Wed, 02 Sep 2020 12:49:24 GMT BitTorrent v2  
<https://blog.libtorrent.org/2020/09/bittorrent-v2/>  
Submitted by RockSteady (TRTL) on Mon, 07 Sep 2020 20:17:16 GMT Shopping Cart — VirMach  
<https://billing.virmach.com/cart.php>  
Submitted by Crappyrules on Tue, 08 Sep 2020 13:20:54 GMT 52Pi Rack Tower 4 Layer Acrylic Cluster Case Large Cooling Fan LED RGB Light for Raspberry Pi 4 B / 3 B + / 3 B / Jetson Nano|Demo Board Accessories| — AliExpress  
Cheap Demo Board Accessories, Buy Quality Computer & Office Directly from China Suppliers:52Pi Rack Tower 4 Layer Acrylic Cluster Case Large Cooling Fan LED RGB Light for Raspberry Pi 4 B / 3 B + / 3 B / Jetson Nano  
Enjoy Free Shipping Worldwide! Limited Time SaleEasy Return.  
<https://www.aliexpress.com/item/4000576747782.html>  
Submitted by l33d4n on Sun, 13 Sep 2020 15:16:07 GMT v/docs.md at master vlang/v GitHub  
Simple, fast, safe, compiled language for developing maintainable software. Compiles itself in <1s with zero library dependencies. [https://vlang.io](https://vlang.io/) — vlang/v  
<https://github.com/vlang/v/blob/master/doc/docs.md>  
Submitted by RockSteady (TRTL) on Tue, 15 Sep 2020 15:44:32 GMT <https://comodosslstore.com/blog/what-is-ssl-tls-client-authentication-how-does-it-work.html>  
Submitted by iburnmycd on Wed, 16 Sep 2020 02:58:14 GMT

![Funny memes by Angel McDaniel on Circle game | Memes ...](https://miro.medium.com/proxy/0*KsIIqvdBmpnW1qjA)

you looked.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-september-16-2020/)_._
