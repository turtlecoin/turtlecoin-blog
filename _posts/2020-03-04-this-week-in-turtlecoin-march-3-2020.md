---
layout: "post"
title: "This Week In TurtleCoin (March 3, 2020)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0yGs8pZdn-6n6dAnG.gif"
date: "2020-03-04T01:58:42.013Z"
---

![]({{ site.baseurl }}/images/0yGs8pZdn-6n6dAnG.gif)

And just like that, it’s like we never stopped posting :)

![]({{ site.baseurl }}/images/06sOKB-MCAogcnTlu.gif)

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

## TurtleCoin Core

After a successful fee per byte fork and a lot of other big changes, there were a fair few requested features and bugs that needed handling:

- The first change was to allow wallet-api to support sending multiple transactions simultaneously. This was not encountered in testing, but with more people adopting wallet-api for their services, it was desired to be able to successfully send many transactions back to back, and before this change, the latter transactions would fail due to using the same funds the first transaction used. As the first transaction was still in the process of being created, the funds had not yet been locked from using in transaction creation.  
  With the latest code, this is no longer an issue, and you can now send transactions as fast as you please.
- The next fix was to handle a bug in the wallet format upgrader. In v0.22.0, zedwallet migrated to a completely new backend, which uses a different incompatible wallet file format. Zedwallet would automatically convert the wallet to the new format, but in some cases, there was an issue where the sync would start at an earlier point in the blockchain than expected. This caused transactions to be scanned twice, resulting in some peoples wallets showing double the true balance. While a simple rescan fixes this issue, we have now prevented double scanned transactions from being counted twice.
- As more service operators have been adopting wallet-api, they desired logging to help track down issues and monitor the operation of services. While both zedwallet and wallet-api already supported logging, this logging can now be easily written to a file, for better integration with monitoring apps, and easier bug reporting.
- Next up, another one for service operators, is a new wallet-api method to allow exporting the wallet data in a JSON format. This can then be easily imported into other libraries, such as turtlecoin-wallet-backend-js, which allows working with the network directly in javascript, without having to use HTTP endpoints which allows for a much richer API. It also helps aid in debugging, as it can let you inspect all transaction inputs and outputs.
- Another change that was introduced in v0.22.0 was threaded validation of transaction inputs, which allows for much higher CPU utilization when syncing blocks. This had the unfortunate downside of introducing a race condition when accessing the database, which could rarely cause crashes. This should have now been fixed by using a thread safe database access method. Make sure to try this one out if you’ve been experiencing random daemon crashes.
- Again on the wallet-api theme, service operators requested further control over fusion transactions. While regular users generally want to keep their wallet comprised of as few inputs as possible, allowing them to send the maximum amount possible with minimum fees, pool owners or other service operators may wish to fuse inputs only up to a certain size, allowing regular payments without locking funds, and transactions with a smaller average size by utilizing primarily inputs of the target output amount. For example, if you regularly send payments of 10,000 TRTL, then you probably want most of your inputs to be around the 10,000 TRTL mark so you use fewer inputs and create less change.
- Finally, we have a fix for pool owners, which may have caused daemon instability when calling certain API endpoints with an unsynced daemon, mainly the /submitblock method. This is now safely handled, and should not interfere with regular daemon operation.

That’s all for this week. If you’re interested in helping out with development, check out the GitHub issue tracker for easy to tackle first issues.

**Zpalm** <https://github.com/turtlecoin/turtlecoin>

![]({{ site.baseurl }}/images/0ZgDvdKE8yKklx8uu.gif)

## Threaded input validation

I was working on another pull request, and to verify everything was working correctly, I needed to do a full sync from zero, without checkpoints. You have to manually disable the inbuilt checkpoints to do this, and it ends up taking an awful long time.

I was checking out my CPU usage, and noticed it was just using a single core, so I set out to figure out if I could speed it up. I started by adding a threadpool class, this lets us run a few threads constantly waiting for work, instead of spawning multiple threads for every transaction to process, which would add a lot of overhead. Once that was done, I just needed to queue up each expensive input validation into the threadpool and wait for them to complete in parallel.

Once done, I was seeing around 30–50% CPU usage, which for my cpu was a speed increase of roughly 4–7x.

The good news is that this improvement also applies when you are syncing new blocks that are not covered by the inbuilt or external checkpoints — so everyone can benefit if they have cores to spare. If not — no problem — you can make it run on just a single thread via a command line option if desired.

**Zpalm** <https://github.com/turtlecoin/turtlecoin/pull/965>

![]({{ site.baseurl }}/images/0vBuNXHbaANc0VoKw.gif)

## **Proton Wallet**

Hey everybody, Extra here, just checking in on the direction that Proton is headed in. I’m pretty excited about some of these planned changes I’ve begun working on.

Some of you (especially those of you with slower machines) may have noticed that when the wallet is syncing, it slows the GUI down to a halt, particularly some of the more spammy blocks. Well, I’ve began the work of extracting the wallet backend out into its own process. What’s this mean? It means that when completed, the GUI and the wallet syncing process will each use their own process on the CPU; so that even when the CPU is working as hard as it can on the wallet sync, the GUI itself should always be fast and responsive. Neat!

I also want to take the time to thank the TurtleCoin community and the hackathon judges on my hackathon win! If you haven’t seen the project I entered, it’s a 3d visualization of the memory pool. It was a fun project for me to do and I’m totally stoked it won out of 20 entries! Check out the link below if you haven’t seen it yet.

Until next time, stay cool TurtleCoin Community!  
**ExtraHash** <http://mempool3d.extrahash.org/>

![]({{ site.baseurl }}/images/0WM6I7vbzDMl5Co7Z.gif)

## turtlecoin-crypto

Long story short, the turtlecoin-crypto project is the stand-alone version of the cryptography used within a number of community products. It supports Node.js, WASM, JS, C++, C# (via P/Invoke) and a few others.

The biggest updates I’ve added lately include full TypeScript definitions of the library and building the wrapper that is currently in turtlecoin-utils into the base crypto NPM package thereby making it even easier to work with the cryptographic package.

**IBMCD** <https://crypto.turtlecoin.dev/>

![]({{ site.baseurl }}/images/0Pbf964h4nqaJNOgb.gif)

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- <https://github.com/turtlecoin/turtlecoin/issues/1025>  
  **#1025 Update user exposed file path opening with error messages**
- <https://github.com/turtlecoin/turtlecoin/issues/1024>  
  **#1024 Prevent importing same wallet multiple times #1024**
- <https://github.com/turtlecoin/turtlecoin/issues/862>  
  **#862 Use matches property in ApiDispatcher regex**
- <https://github.com/turtlecoin/turtlecoin/issues/811>  
  **#811 Remove no longer relevant asserts**

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

![]({{ site.baseurl }}/images/0TenLdTuFficN7ZuD)

This week’s rig, “w1” @ 249 kH — TRTLv3iLkDhPvHYigBwMwv5714t54w6M833cVuQCYKiCTJ3UowAChbV1nBfTcU1XkaJaeAUyQYQqqQdGWobWjkMLH4A4QAoYJo3

![]({{ site.baseurl }}/images/0IE7Cvhszcvk2GjtP.jpg)

It’s free!

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- Don’t sleep on MuxDux Mining Pool. And join our Discord group to speak with other grassroots miners. [http://trtl.muxdux.com](http://trtl.muxdux.com/)
- TurtleCoin shrimp and animal farm — more games and faucet in the making <https://trtlfun.com/>
- harrynetwork.uk.to:11898 The Cheapest TRTL Node — only 2.5 TRTL fee! <https://explorer.turtlecoin.lol/nodes.html>

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- **Neo_Chen** Mom, I am on TV!
- **greywolf** thanks to LeoCuvée for recommending switching from using a micro sdcard to using an ssd via usb3 to store blockchains locally on my Macbook.
- **Jaoakar** Thanks for being You! To another great year of turtlecoin.
- **greywolf** thanks again to zpalmtree for always stepping up to help a struggling turtle who does not understand code but is immersed in the land of code-writers.
- **greywolf** i apologize to RockSteady for egging on a heated discussion in his server that started in a different server, and i should have dropped it. instead, i came into the TurtleCoin server and continued the argument, which was not the right thing to do. Rock wears the crown, so i was out of line.
- **greywolf** thanks a lot to zpalmtree and ExtraHash for helping me set up windows and linux testnets. and also thanks a bunch to Crappyrules for a one-on-one tutorial on the internal checkpoints file of the core code. i really appreciate these guys explaining stuff to me in a way that i can undrstand.
- **japakar** thanks!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-3-2020/)_._
