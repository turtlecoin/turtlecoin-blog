---
layout: "post"
title: "This Week In TurtleCoin (FEB 19, 2019)"
description: "TurtleEDU — Thanks to all of the students who have submitted spelchex and currectshuns forr TurtleCoin 101 :) Fexra and I have had a fun time hunting down errors and resetting passwords. The email…"
image: "{{ site.baseurl }}/images/0Hsh017ty9hmkxKsD.png"
date: "2019-02-19T22:58:42.932Z"
---

![]({{ site.baseurl }}/images/0Hsh017ty9hmkxKsD.png)

Two roundups in three days, who knew we’d be so lucky! Back on schedule!

# Developer Updates

![]({{ site.baseurl }}/images/0T3iodEY9BmRHDwfQ.png)

**TurtleEDU** — Thanks to all of the students who have submitted spelchex and currectshuns forr TurtleCoin 101 :) Fexra and I have had a fun time hunting down errors and resetting passwords. The email system is still kind of a joke (it uses a gmail integration that worked one time, we swear), so please write down your passwords until we figure out something to fix it. A lot of you have been asking about when followup classes will be ready, and I’ve begun gathering information about what people want to see in the Beginner’s Git class which goes over the Git version control tool we use. If you have suggestions relevant to the Git class, please post them in #edu_general. Since the goal of the first class was to turn people into competent TurtleCoin users, the goal of this next class will bring everyone to the level where they should feel comfortable contributing on Github, which as you may know is how you get your pink “Contributor” role in Discord. — **Rock**

[http://edu.turtlecoin.lol](http://edu.turtlecoin.lol/)

**Turtle Swap Protocol Whitepaper** — I had the chance to speak with Napoleon (from TRTL and VELD) and we’re fleshing out some of the concepts laid out in the Turtle Swap Protocol Whitepaper as it appears he’s been working on developing a similar concept for Veldspar. The concept aims to enable wallet to wallet transfers of multiple currencies without touching an exchange, and in this case it’s particularly interesting as it’d involve a swap outside of a cryptonote network. I’m hesitant to call them atomic swaps just yet, but the whitepaper gives the gist of how it’d function at a conceptual level. We’re looking for other devs to collab with on developing the next draft of the whitepaper, so if you’re the type of person who’s interested feel free to stop by the chat in #dev_general or create an “issue” in the turtle-labs repo. **— rock**

[turtlecoin/turtle-labsPublications and Research Efforts. Contribute to turtlecoin/turtle-labs development by creating an account on GitHub.github.com](https://github.com/turtlecoin/turtle-labs/blob/master/Turtle-Swap-Protocol-Draft-001.md)

![NPM](https://miro.medium.com/max/60/0*jNyZ0vKuqjvwHYSX?q=20)

![NPM](https://miro.medium.com/max/754/0*jNyZ0vKuqjvwHYSX)

**Node.js Goodness For TurtleCoin —** Some of you may know about the TurtleCoin Utilities package that Zpalm and I have been working on to make it very easy to perform a lot of the CryptoNote cryptographic functions in Javascript.

The TurtleCoin-Utils package can be used in browser, in Node.js, react-native, and has TypeScript bindings available.

Using this package, it’s very easy to create new wallets, encode addresses, decode addresses, handle integrated addresses, scan transactions for your funds, create new transactions, and etc.

This package is very powerful and provides a nice way for those looking to get started in TurtleCoin development easy to follow source code that guides you along the way. It is also part of the foundation of TurtlePay payment processing and is used heavily by Zpalms’s wallet backend in JS.

Running all that crypto can be a bit slow in raw JS, but no worries, help has arrived.

![NPM](https://miro.medium.com/max/60/0*z6BFloWK2DOfmZIc?q=20)

![NPM](https://miro.medium.com/max/754/0*z6BFloWK2DOfmZIc)

The TurtleCoin Crypto module for Node.js is a native C++ addon for Node that provides significantly faster cryptographic routines for use with TurtleCoin-Utils and other packages. It is very generic in handling CryptoNote related cryptography so many projects besides TurtleCoin may find good use of it. It exposes a lot of the underlying cryptography that the TurtleCoin Utilities needs as well as a few extras.

The TurtleCoin Crypto module is automatically loaded as an _optional_ depenedency for TurtleCoin Utils which has the utils package us it for the crypto (30–40x faster than the native JS code) and falls back to the native JS if necessary.

**TurtlePay Updates** — We’ve been working hard implementing some updates to underlying packages (see above) to speed up the processing of the one-time wallets. In addition, we’ve been working on extending out some of the functionality of the blockchain API to support additional endpoints that provide the necessary data for working with additional wallets like Zedwallet++, wallet-api, walletbackend-js, and the mobile wallet that Zpalm is working on.

Recent updates also include better callback message signing that makes it a lot easier for developers to verify that the callback message(s) that they receive from TurtlePay were indeed generated by TurtlePay.

**Multisignature Wallets** — I’ve been working pretty diligently the last few days to prepare the underlying cryptographic functions and primitives necessary to bring multisignature wallets to TurtleCoin. This is one of those features that make it easier to perform advanced wallet services that provide extra security for your funds. The cool thing about it is that there are no changes required of the network to support Multisignature transactions so implementing and testing this is entirely wallet side.

More updates to come in the coming days and weeks as I get closer to having something more worth sharing. You’ll probably see me in the development channel throwing chairs until this is finished :)

**turtlecoin-nodes-json** — I’ve removed 32 unreachable nodes from the public nodes list. This should make using applications, that pull from the list, a little more user-friendly. I wrote a script to poll public node availability and used the results from a period of 12 hours to determine which nodes would be cut. I only removed nodes that were 100% inaccessible. If you feel your node was removed in error, please check that your node is publicly accessible and create a pull request to get it back on the list. To ensure your node is reachable you can use the netcat command on linux (e.g. netcat -vz mydomain myport) or use one of the many websites that checks for open ports. **— andrew | trtl.rocks**

[turtlecoin/turtlecoin-nodes-jsonjson list of public daemons. Contribute to turtlecoin/turtlecoin-nodes-json development by creating an account on…github.com](https://github.com/turtlecoin/turtlecoin-nodes-json)

![]({{ site.baseurl }}/images/0iNFZWwJxvvkNn3dI.png)

**Thinkpol’s TRTL Tetris!** — This one was submitted via the chat but was pretty awesome so i had to show you guys. One of our users on the TurtleCities server, Thinkpol, created this awesome TurtleCoin Tetris game on his TurtleCities homepage, and coolest of all he did it with less than 2.88MB of storage space for the entire site. Just in case some of you don’t know, TurtleCities is like our free GeoCities replacement for the old fogies in our crowd who remember that place. If you want to see some of the pages others have made, check out pages.turtlecoin.lol

[TurtleCoin TRTRISEdit descriptionpages.turtlecoin.lol](http://pages.turtlecoin.lol/~thinkpol/)

**Javascript Wallet Backend** — Hello, If you are a developer, you have probably interacted with turtle-service. It works well, but sometimes you need a little more fine grained control to give better error messages, and not have to worry about firewalls blocking your connection to the RPC. Enter <https://github.com/turtlecoin/turtlecoin-wallet-backend-js> This provides the same sort of functions as turtle-service, however, it is written in Typescript, and so can be easily used in both TypeScript and JavaScript environments. You can use this instead of turtle-service to build wallets, and other services. It should give a better level of integration, allowing your program to be more user friendly. A simple example is it offers events, which can make your code easier to read, and saves you having to check the status of the wallet every N seconds.

wallet.on('incomingtx', (transaction) => {  
console.log(`Incoming transaction of {prettyPrintAmount(transaction.totalAmount()} received!`);  
});

It also adds a number of utility functions, such as formatting atomic amounts, validating addresses, and much more. If there’s something you’d like to see that’s missing, I’ll be happy to add it.  
Thanks to iburnmycd, it now automatically includes support for speedy C++ cryptography, and so wallet syncing speed will be similar to turtle-service, rather than having to use slow JavaScript.  
The backend also supports the TurtlePay blockchain cache API — This works just like a daemon, but has much better uptime, and can also speed up wallet syncing.  
One thing I haven’t got to yet is adding support for fusion transactions, but this will be pretty easy. If you’re wanting to use them, give me a ping, and I’ll get them added. **— Zpalm**

# Promote Your Bounty

1,500,000 TRTL — Cryptonight Soft Shell GPU miner integration with pool compatible mining software. — Hooftly

# Community Advertisements

[https://trtl.muxdux.com](https://trtl.muxdux.com/) — Mine with Muxdux. We are a small pool trying to get a little bit bigger. Join our active discord channel (<https://discord.gg/QJ37K9Q>)

# Shoutouts & Thanks

rock — Thankful for the TRTL core team putting in work around the clock to bring us new features and goodies. Also thankful for all the communities around us that lend us their users for diabolical testing fun and games and their devs that help us achieve our goals. Thanks to everyone who helped us get here.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-feb-19-2019/)_._
