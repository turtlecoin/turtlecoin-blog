---
layout: "post"
title: "This Week In TurtleCoin (OCT 23, 2018)"
description: "turtle-completo — I have rewritten the local turtle explorer using python and kivy frame work. Initially I just wanted to find a good GUI framework to make a turtle wallet, then I was looking into…"
image: "{{ site.baseurl }}/images/0ITCzAktAQmdAF8c5.png"
date: "2018-10-23T16:12:47.568Z"
---

![]({{ site.baseurl }}/images/0ITCzAktAQmdAF8c5.png)

# Developer Community

**turtle-completo** — I have rewritten the local turtle explorer using python and kivy frame work. Initially I just wanted to find a good GUI framework to make a turtle wallet, then I was looking into kivy for its crossplatform feature. So I thought I could move the local explorer to kivy first, then start developing the turtle wallet that I wanted to add on to the local explorer. The turtle-completo project looks better and it is more dynamic in terms of searching behavior, and it is faster than the previous local turtle explorer, though I know there is still a lot room for improvement. (I admit my code is a bit messy, and I probably forgot to remove some unused lines, I will get back to that later and clean it up) The turtle wallet is still under development. If anyone that wants to join the party and make a “project completo” with me, just DM me on discord. Also, if you are developing or interested in developing a mobile version turtle wallet, please let me know, I would like to work together. **— Sabo (Revolutionary)**

[yumingchangsabodota/turtle-completoturtle local explorer (turtle completo). Contribute to yumingchangsabodota/turtle-completo development by creating an…github.com](https://github.com/yumingchangsabodota/turtle-completo)

**turtlecoin-rpc-go —** 2 weeks back I posted about the major restructure that this library (turtlecoin-rpc-go) got and I told about the documentation thing. Here we are today, in this timespan I have tested every RPC call using the library and documented those at [https://api-docs.turtlecoin.lol](https://api-docs.turtlecoin.lol/) . The library also got some error handling as promised. It is up to date with the latest dev branch of the network. I will be working on adding more error/exception handling, making it more reliable (which it is by the way), and follow the Go standard conventions. I am looking forward towards the community to integrate this library in their projects. **— rashedmyt**

[turtlecoin/turtlecoin-rpc-goA Golang wrapper for the TurtleCoin RPC API. Contribute to turtlecoin/turtlecoin-rpc-go development by creating an…github.com](https://github.com/turtlecoin/turtlecoin-rpc-go)

![]({{ site.baseurl }}/images/0p0aGxzGvF3SVGlts)

**GUI Node** — I got the gui node working with the help of Z and ibmcd. The purpose of the GUI node is that home users need to be able to run public nodes on their home computers to avoid centralization with AWS and other cloud providers. A simple port forward is all you need. The chain is getting big enough to where it makes sense to run on home hardware rather than a hosted server. Currently you can start the daemon and define a price and fee wallet. The roadblock I’m having is kind of stupid. I’m trying to assign the value of the fee when entered to the QProcess parameter. It sounds really simple but I’m just dumb when it comes to Qt. -Rock

**Web Wallet —** Now that we’re at a point on our fork that we can release, we’re shifting focus back to the web wallet. In progress at the moment is the ability for the webwallet to connect directly to a node (private node). The first step of this is to create some new RPC calls in the daemon to allow the web wallet to retreive transactions directly (thanks @ZPalmTree who’s already done some work on this), this involves some optimisation and stripping of data we don’t need and then we will update the web-wallet’s RPC calls to go direct to node so we can drop the background caching process in the web wallet. The final challenge with this is to ensure that the web-wallet, on an HTTPS interface can connect directly to the node on an HTTP interface. -**WhassupZA | Plenteum**

[turtlecoin/turtlecoin-webwallet-jsTurtleCoin Clientside Web Wallet. Contribute to turtlecoin/turtlecoin-webwallet-js development by creating an account…github.com](https://github.com/turtlecoin/turtlecoin-webwallet-js)

![]({{ site.baseurl }}/images/0dU-F1bTomrjQdykN.png)

**billionTRTLhomepage —** The billionTRTLhomepage is a place where you can place ads and get seen. The screen is split in 10000 fragments and you can rent some of them and display your ad there. Payments are made with TurtlCoin. We have over 120 active user from all over the world. **— fipsi#0789**

[Billion TRTL Homepage - interesting offer - place adsbillionTRTLhomepage - view the newest products and opload your own ads - pay with cryptocurrency - 1000+ unique…www.billiontrtlhomepage.lima-city.de](https://www.billiontrtlhomepage.lima-city.de/)

# Community Advertisements

![]({{ site.baseurl }}/images/0SSurVi6n2FSGFG9r.png)

- Celebrate the TurtleCoin Network with us by syncing your GUI or CLI wallet with turtlenode.online! With our new competitive TX charges, you’ll never need another node again, it’s simple! Satisfaction guaranteed, or your money back!\* “Switching to turtlenode.online made me feel great” — Anon. \*Money-back offer includes TX fee’s only. Terms and conditions apply. Please visit [http://chat.turtlecoin.lol](http://chat.turtlecoin.lol/) for more information
- Turtlecoin decals for sale, in variable sizes and colours. Payment either via Trtl or PayPal. Look me up on Turtle Discord Judderz#6983

![]({{ site.baseurl }}/images/0D21RsZHScNAdxa_O.png)

- billionTRTLhomepage — a place where you can rent ad space and get a audience of 100+ visitor per day
- pubnodes.com offers Public Nodes for 5 Cryptonote Variants currently and is expanding. Currently the coins offered are Turtlecoin, Monero, Masari, Nerva and Blur Network. The goal of this project is to provide a quick, easy and private way to broadcast transactions to the coins respective blockchains with minimal effort. To enhance transaction privacy all Nodes are offered as .onion hidden services allowing you to broadcast transactions without leaving the Tor network. This is ultimate Transaction Privacy. This service is free and always will be so please drop by. [https://www.pubnodes.com](https://www.pubnodes.com/) \-Hooftly
- 5 fee Turtle Nodes! turtle.japakar.com Germany location 35.199.160.13 US West Location Thanks for using the nodes!
- Come and join to turtle.casa mining pool!

![]({{ site.baseurl }}/images/0jjJiQnX-LNjOI_fs.png)

- <https://perspectivecoffeeco.com/new-products/>

# Bounty Listings!

**100,000 TRTL —** Looking for a “Hunter” turtle design logo. The style of the design can range from the stereotypical “Safari Hunter” look to a badass tribal Hunter turtle. -Xaz

**20,000 TRTL** — Make a turtle dab emoji -Sajo8

**10,000 TRTL —** make a guide on how to mine trtl on an iphone with “XMR Miner”. Must follow format of the existing ‘mine on your phone’ guides. -Sajo8

# Shoutouts & Thanks

Poike Stompers#3053 — You guys do an amazing job out there!!

Sabo (Revolutionary) — Everyone go use the turtle-completo local explorer! Be a turtle node, explore locally!!

anon — shouts to rashed and sajo for being awesome

anon — crappy we miss you

aseriousgogetta — Shillin’ These Shells.. It’s What I Do

anonymoose — IBurnMyCD is cool

rock — shouts to scarabey, looking forward to your blog

rock — thanks to watter for the interview

Barelycloakedish — Shoutout to @Rocksteady for some kickass motivational speeches. Thanks for being the coach we need in our locker room.

anon — alien we love you, even if we cant show it

rashedmyt — Huge shoutout to dsanon for using my RPC package in his webwallet shellnet.pw which is TurtleCoin’s first production ready webwallet..

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-oct-23-2018/)_._
