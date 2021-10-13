---
layout: "post"
title: "Interview w/ WhassupZA from Plenteum"
description: "OK great, thanks for doing the interview. I understand that you came across the TurtleCoin/Masari web wallet porting project because you yourself operate a TurtleCoin fork known as Plenteum. Since…"
image: "{{ site.baseurl }}/images/0NAjSs84_FpKumjIr.png"
date: "2018-10-15T10:22:34.018Z"
---

![]({{ site.baseurl }}/images/0NAjSs84_FpKumjIr.png)

# RockSteady (TRTL)

OK great, thanks for doing the interview. I understand that you came across the TurtleCoin/Masari web wallet porting project because you yourself operate a TurtleCoin fork known as Plenteum. Since Plenteum was the motivator behind porting this web wallet, can you tell us a bit about the vision behind it, and where the fork is headed?

# WhassupZA | Plenteum

It’s a pleasure, thank you for giving me the opportunity to talk with you. Plenteum is a project I started a few months back, I have had an interest in the technical aspects of Crypto Currencies for a long time now. Initially I was just looking at various coins source code and trying to figure out how it all worked purely for my own interest.

As I got deeper into the technology, and did more reading, an idea struck me. Without getting into too much detail, and as you probably already know, a number of existing blockchain implementations have the problem of Dust. It causes users wallets to get clogged up, which in turn causes the cost of transactions (fees) to increase, it also adds additional load on the network. Coupled with that, there has been speculation, or concern that transaction fees alone will not be enough to sustain the incentive for miners to continue mining once coins enter their tail emission phases, or the emission runs out entirely. So, I thought that with Plenteum I could offer a potential alternative to funding future mining rewards, and reduce the amount of DUST in the blockchain.

By extracting dust from the users wallets when they send transactions (as a replacement for fees, and only where there is dust to extract) we could then use that to build up a “Dust Fund” over time, which would then become the basis for future mining rewards when the coin enters it’s tail emission phase. This has the added benefit that mining rewards can also be more consistent than pure fees would be, as with fees, how much the miner earns for each block is dependant on what transactions are added to that block that the miner submits. With the Dust Fund, we can calculate a consistent reward that is based on transaction throughput over a longer time period, allowing miners to more accurately calculate what they might earn from mining.

# RockSteady (TRTL)

That’s interesting as a concept with dust. How would this affect pools, faucets, and micropayments who are the chief creators of dust? Would this end up in a network that is more geared toward large transactions? How does the ability to fuse inputs affect this?

# WhassupZA | Plenteum

The thinking at this stage is that dust will be extracted from outputs on transaction send, due to the cryptographic elements, we cannot “alter” transactions once they’ve left the users wallet, so the idea is to take the smallest 6 units out of the transactions outputs when any user sends a transaction, be they a pool, faucet or standard wallet user and redirect those to the dust fund. Under the hood, the coin itself operates on 8 decimal places, but only 2 are useable, so the remaining six would make up the dust. By way of example, if I sent you 23.25 PLE, this would be made up of up to 10 outputs, 8 behind the decimal point and 2 in front of it. (essentially the amount might be something more like 23.25760213). We are then redirecting the lowest 6 decimal places, so you still receive 23.25 PLE, the initial wallet owner has not paid any fees, but has contributed to the Dust Fund from the “fused” outs that make up the smaller amounts. So when that TX hits the receivers wallet, there are less outs for them to fuse into future transactions. So it should not affect fusing inputs, and not necessarily only geared towards large transactions, but is dependent on there being a significant number or volume of transactions going through the chain. The more “divided” each transaction is, the more Dust there should be.

Just as a side note, we are not removing fees entirely, they will become non-mandatory as we felt users should still have the ability to push transaction priority up should they so choose. We also did not want to make changes to the extent that miners would be required to have custom mining software etc. So we’re aiming to do this as a simple change initially, and then allow community feedback, results of early operation etc. to inform how it progresses from there

# RockSteady (TRTL)

That’s a pretty cool idea, I can’t wait to check it out. You seem pretty capable, and in fact you’re the first fork to contribute something back upstream. Can you tell us a bit about your background in programming, and maybe tell us about what drew you to the crypto space initially?

# WhassupZA | Plenteum

Why thank you

I have gained so much knowledge, assistance, help etc. from so many over the years that I’ve always tried to remain conscious of giving back, or paying forward. When I settled on TurtleCoin as the coin I wanted to fork, I wanted to make an effort to give something back to the turtle community (which I’ve been a small part of since February or March 2018, albeit as a miner / user and not a dev) .

I started programming when I was in my teens (I’m now in my early 40's), I’ve always had an interest in tech, and love a good challenge. Initially as a youngster I thought I wanted to study Accounting and I took Computer Science as a “filler” during my degree. The bug bit and I haven’t looked back. Since then, I’ve worked as a custom software developer in various agencies. I’ve largely had a web based focus over the years, and my experience is predominantly on the Microsoft Technology Stack (ASP.NET, C#, SQL Server etc.) but have dabbled in Java, Delphi and a few other languages over the years. What drew me into the Crypto space was really just a personal interest, I love new toys, and I love technology. I wrote a paper in my Honours year at University titled “Towards a Model of an Electronic Cash Payment System for Business to Consumer Electronic Commerce”. This was a primitive (with hindsight) attempt to come up with a model that Blockchain has essentially solved today — my model was nowhere close to Blockchain, but it sparked an interest while doing all the research and I’ve tried to keep up with developments in the Crypto world.

# RockSteady (TRTL)

That’s pretty much the perfect recipe for “Guy-who-ports-webwallet-for-obscure-codebase” if that’s what you were shooting for when you went to school all those years ago

So tell me more about your work with the web wallet. For those who aren’t familiar with which web wallet we are talking about, WhassupZA is porting the Masari Web Wallet that Gnock made. It is special because it is a trustless, safe, completely clientside web wallet, which means the owner/operator of the web wallet can’t run off with everyone’s keys, and there is no risk other than inconvenience if the web wallet goes down.

Now that we got that little primer out of the way, can you tell us a bit on some of the changes you’ve made? Currently, Masari is a Monero-based network, and though Monero was originally based on Bytecoin, like us, they have evolved significantly since forking, just like us, so a bit of squeezing in some places was required for us to be able to use it. Would you like to talk about the changes you’ve made and which ones were required vs which ones you added to improve on what was there before

# WhassupZA | Plenteum

The first thing I looked at was the background caching and client sync process, I was aware when I started that the JSON output of transactions from a node on our code base would be slightly different to what Masari’s looked like, but found a few things I wasn’t expecting. So I set about breaking down the processes of syncing and caching and extracting everything we needed in a transaction in order to sync a wallet. The main difference (aside from the structure of the JSON output) was that Masari uses RingCT, which we do not, so we needed to change the way the transaction ownership was verified for the currently active wallet. I managed to get that out the way fairly painlessly, and then moved on to raw transaction sending. That was a whole different kettle of fish for me. I set about stripping out RingCT signing from the existing masari code, reworked the Tx Extra structures to match what we had in our Tx’s and then started looking at the construction and signing process. I struggled to find anything online (and ultimately did not) that would point me in the right direction for how to piece together a transaction outside of the core software itself.

Ultimately it was a case of trial and error, I manually broke down a few transactions into their individual parts, and ultimately found the error I’d made in the process of removing RingCT and sent my first successful transaction from the web wallet. Had you been in the room with me, you might have thought I’d won the lottery or something I was so excited🤣

Once I had the wallet sync’ing and was able to send transactions I moved on to optimising the sync process, made some minor styling and layout changes and started looking at how and where we could improve things.

I also built a Web Socket proxy to allow mining from within the wallet, but we decided to remove that. I am currently working on some enhancements to how “pending” transactions are handled and displayed (these are transactions in the mempool, as well as un confirmed transaction) and am also working on a change to show fusion transactions that still need to be confirmed. Once that’s done, I will look to add the ability to send fusions (optimize your wallet).

# RockSteady (TRTL)

You’ve done so much in so little time, are you grinding this out alone or do you have help? Is the Plenteum community already testing out your fork of this, or are you waiting to deploy it until those last few action items are knocked out?

# WhassupZA | Plenteum

I am working alone at the moment, mostly in my spare time as I also have a day job, but am actively looking for dev support, so if you know of anyone who might be interested, please ask them to contact me :-). We have a beta wallet setup for both Plenteum and Turtle’s wallet instance (although I’ve taken turtle’s offline temporarily as I need to move the git repo and resync the chain following some optimisations). A few people have had a go and reported back a few things that I’d ideally like to get fixed before it gets deployed. These are mostly minor things, that don’t affect the ability to operate the wallet, but may create some confusion for end users. For example, when the wallet displays a pending transaction that’s in the mempool, it shows up in the transaction list, then, when it’s removed from the mempool and added to a block, it disappears from the transaction history for a minute or two as it’s added to a block. The background caching process will not yet have picked up that block and then it can take a few minutes for that transaction to re-appear in the wallet having been added to a block, but yet confirmed. So that has confused a few testers and we need a way to improve that.

I haven’t opened up the beta to everyone in the Plenteum Community, but have invited a few users from Plenteum and a few of the TurtleCoin dev’s and contributors for an initial look at each

# RockSteady (TRTL)

It’s ok

After you’ve got the wallet up and running for your first beta release, do you have plans to extend the functionality any? You mentioned breaking off the web miner, which I think is a good idea, do you plan on making that a standalone deployable tool for web miners?

# WhassupZA | Plenteum

The longer term vision for the web wallet is to make it the foundation for all wallets for all platforms. Using Cordova for mobile, and Electron for cross platform desktop applications the web wallet gives us the opportunity to have a single code base for all wallets (other than the cli and service wallets), which is a great advantage from a maintainability perspective. I’d ultimately like to add the ability for the web wallet to connect directly to a node, and not have the background caching process, which will let users connect their web, mobile or desktop wallets to their own node, which will greatly improve sync speed and add that extra bit of security. This is difficult for the web interface, as it will operate over https while a nodes RPC interface is over http so a bit of trickery will be required to get that working. I’ve had a couple of initial conversations with Gnock, who’s aiming at the same approach longer term and has made some progress on this aspect so I probably have a few things to learn from his experience with that before I tackle it.

The web miner is definitely something we’d like to work on as a stand alone project. I think it would be a great tool to introduce new people to mining without having to outlay on hardware. Also, for those community members who want to donate, they could point their CPU at the web miner and help the project along, while also contributing to the network decentralisation, which would be fantastic

# RockSteady (TRTL)

Good idea. I like the idea of keeping web miners around. I think they can be a great tool, as long as they are being used with the user’s permission at all times. Is there anything on the roadmap for Plenteum or TurtleCoin that you have up your sleeve?

# WhassupZA | Plenteum

Agree 100%. We do have a couple of use cases we are working towards with Plenteum, but they’re dependant on a few other things falling into place first, so I’m playing those cards close to my chest for now. I am also weary of over promising, I think far too many coins shoot for the stars and barely get off the ground, so I’m just trying to keep things realistic for now.

As far as TurtleCoin is concerned, I’d love to continue contributing. I have started digging around in CantiLib (the dot net re-write of the core software for those not familiar) and am very keen to contribute to that as much as I am able.

Other than that we’re working on building our community and just keeping things moving forward in general

# RockSteady (TRTL)

I think the community is going to really enjoy this interview, thanks for your time and the depth of your answers. Is there anything you’d like to add before we wrap it up?

# WhassupZA | Plenteum

Thank you! I’ve thoroughly enjoyed chatting with you and looking forward to seeing it published. Nothing extra to add from my side, just to say I really do appreciate it

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/interview-w-whassupza-from-plenteum/)_._
