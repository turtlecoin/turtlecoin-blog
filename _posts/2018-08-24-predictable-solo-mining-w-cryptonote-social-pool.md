---
layout: "post"
title: "Predictable Solo Mining w/ Cryptonote.Social Pool"
description: "Decentralizing the network hash rate is important, so that any one pool owner going rogue or a single server breaking doesn’t also tank the rest of the network. The purpose of this new series is to…"
image: "{{ site.baseurl }}/images/0O9IOdmf84BVKwdPe.png"
date: "2018-08-24T13:17:43.537Z"
---

![]({{ site.baseurl }}/images/0O9IOdmf84BVKwdPe.png)

_Decentralizing the network hash rate is important, so that any one pool owner going rogue or a single server breaking doesn’t also tank the rest of the network. The purpose of this new series is to encourage the decentralization of mining power by highlighting unique pools that are coming up in the TRTL mining biz. Choosing a smaller pool helps the network secure your assets by not giving any single person enough power to call the shots for you. Thanks for choosing to balance the hashrate, and I hope you enjoy the interview :) — RockSteady_

**RockSteady** — So tell me, how did you get started in mining? What’s your origin story?

**cryptonote.social** — I started mining Bitcoin back in … oh, I don’t remember exactly, but it [was worth about $50 at the time. 2013?](https://www.buybitcoinworldwide.com/price/) I came across [Satoshi’s whitepaper](https://bitcoin.org/bitcoin.pdf) and was blown away. I’d been dabbling in decentralized systems since the 90s, and this was the first piece of work that I had come across that offered a fully decentralized solution to a significant problem, and it did so with such elegance. Of course I had to give mining a try, [even though ASICs were soon to invalidate my efforts!](https://www.digitaltrends.com/computing/what-is-an-asic-miner/)

**RockSteady** — Ah interesting, what were your interests regarding decentralization before bitcoin?

**cryptonote.social** — I’d long been interested in privacy preserving technologies … [cypherpunk](https://www.activism.net/cypherpunk/manifesto.html) type of stuff, though I’d never really fully immersed myself into that community. Decentralization was always a big part of that. I have to say though, what really piqued my interest was the advent of Napster, and seeing how easily it and other approaches were defeated because of their centralized elements and failure to solve trust minimization.

**RockSteady** — That’s cool to hear about. A lot of the people doing things differently now have similar roots. I get that same feeling when looking at your mining pool. It’s a bit different than others. Did you write it from scratch?

![]({{ site.baseurl }}/images/0qlgks1HopHrLVItn.png)

**cryptonote.social** — Yes, I’ve written the bulk of it from scratch, with some help from a small group of friends. I find the best way to learn about a new technology is to just go and build it, and writing code is something I really enjoy. My software admittedly lacks a lot of the bells and whistles of the established node-based pools out there, but it lets me experiment with new ideas and scratch my software development itch. And those who are using it (a small but loyal group) seem pretty happy with it so far.

**RockSteady** — That’s cool! What’s it written in, and what was that like? Did you have experience with [nodejs-pool](https://github.com/Snipa22/nodejs-pool) and [node-cryptonote-pool](https://github.com/zone117x/node-cryptonote-pool) before?

**cryptonote.social** — The backend is entirely [Go (aka Golang)](https://golang.org/) and the frontend is Angular. Go has been my language of choice for the past few years — I find it the perfect language for building servers. [Angular](https://angularjs.org/) is something I was not familiar with until I started this project, but I decided it would be cool to learn. It’s a bit of an over-engineered mess, to be honest, but I suppose overall I’m happy with the results.  
Re: [node-cryptonote-pool](https://github.com/zone117x/node-cryptonote-pool), no, I’d actually never run any pool before starting this. I’d played with a few mining proxies, about the extent of it.

**RockSteady** — Golang is something we’ve been fairly interested in, [and a few of us have begun porting over the turtle libs over; I think Rashed is running that effort.](https://github.com/rashedmyt/go-turtlecoin)  
So your pool is fairly unique in comparison to others and I think that’s given you some good opportunities to implement features other pools might not have. Can you tell us a bit about the special spice that sets you apart?

> “Predictable solo mining originates from EthPool.org, a mining pool for Ethereum. … Predictable solo mining aims to eliminate the risks of never earning anything, which is an unfortunately typical outcome of solo mining.”

**cryptonote.social** — There are a few things, but the main differentiator is probably our predictable solo mining payment scheme, which we’ve begun switching most of our pools over to. Our TurtleCoin pool has been using it for a few weeks now.  
Predictable solo mining originates from EthPool.org, a mining pool for Ethereum. I found it pretty fascinating when I’d learned about it given that running a small pool is basically the same thing as solo mining until you get enough miners onboard. Predictable solo mining aims to eliminate the risks of never earning anything, which is an unfortunately typical outcome of solo mining.

**RockSteady** — Can you elaborate a bit from a high level how you’re able to offer predictable solo mining?

**cryptonote.social** — Well first of all we don’t offer perfectly predictable payouts: the level of predictability still depends on the size of the pool, and one can’t fully eliminate the randomness of the mining process without taking on a lot of risk (e.g. PPS pools). The goal then is to improve predictability in a way that doesn’t involve taking on big risks. The basic idea of our predictable solo variant is to “bank” mined blocks as they come in, and hand them out to miners only when they have computed a number of hashes equal to (actually slightly larger than) the network difficulty. This is a bit different than how EthPool does it, by the way, and we’ve found it actually works reasonably well even when the number of active miners is relatively small.

**RockSteady —** Ah ok. Would this change as it scales? As the pool grows, and gains blocks with greater frequency, does this eventually scale into salaried mining?

**cryptonote.social** — Dynamics actually improve as it scales. The biggest worry is long “droughts” of no blocks, which can really throw things out of whack. This is one reason we actually require miners to hash a bit over network difficulty before earning a block. With a large pool, the chances of long droughts goes down quite a bit.  
There is of course the opposite problem: that you end up with so many blocks in the bank that they just sit there and miners can never win them. Though this situation is rare, when it does happen, we solve it by simply selecting a banked block at random and paying it out in full to the particular miner that actually minted it. Though this goes against the goal of predictability, it’s an infrequent thing, and miners don’t usually mind some small chance of occasionally “winning the lottery” in this way.

**RockSteady** — That sounds fair, I’m impressed. What struck you about the ETHPool paper that made you say “you know what, I can do this a little bit better!”

**cryptonote.social** — [I didn’t actually realize at the time that EthPool had issues,](https://fc18.ifca.ai/preproceedings/79.pdf) and I set out to build exactly what they had done, [only for my favored CryptoNote coins instead of ETH](https://cryptonote.social/trtl). It wasn’t long though that I realized for a pool with one miner that is much faster than the others (a common case for small pools), the scheme was an utter disaster… the fast miner gets all the rewards, nobody else can ever earn anything. Shortly after that I came across an academic paper that outlined other flaws with the scheme affecting even large pools, so I set out to see if I could fix them.

**RockSteady** — Have there been any stumbles or mistakes along the way or has it always been a home run for you

**cryptonote.social —** Oh there were definitely stumbles. We didn’t implement the difficulty margin (having to go a bit over difficulty) initially and as a result the “whales” were running away with most everything. Even after implementing it, it takes a while to get the margin value dialed in. The proper level depends on how variable the network is.  
So for a coin like TurtleCoin where difficulty has big swings and orphans are common, it turned out we had to set it far more generously than we initially guessed. This made some of the smaller miners lose out, and some dropped out for good. I think we have it properly dialed in at the moment, but I would not be surprised if there are some other details we may still need to address. I’m still thinking about other things we can do to better deal with difficulty variance, for example.

**RockSteady —** It’s always a bit tough starting out with something new, but I’m glad that you’re getting dialed in. What do you have planned for the near future with the pool and what are some distance goals you have?

**cryptonote.social** — I’ve been bouncing around a few different ideas. The domain name was chosen because I originally wanted to build a community site of sorts for privacy coin enthusiasts, but once I started with the pool it kind of became all consuming. I do in general like social elements such as the leaderboard, which is why it’s a bit more prominent in my site than you’ll find on most others, and also why all my pools require a username.  
I also have some more out-there ideas around turning the hash power you contribute into a “meta currency” of sorts that you can exchange for actual cryptocurrency on demand rather than having to choose the specific coin ahead of time. But in the short term it’s likely I’ll just continue building out the basic feature set of the existing site.

**RockSteady** — That’s pretty cool! I’m glad you’re branching out into new territory! What’s the best way that the community can contribute?

**cryptonote.social** — At this point it’s mostly just by providing feedback around what I have, though I probably wouldn’t turn away anyone who might want to help pretty up the site a bit as web design is not my strong suit! My code isn’t yet in good enough shape where I’d be comfortable dumping it on github in order to solicit development help, but it’s something I’m working towards. Plus I want to get a better idea of where I want to take all this. I don’t think the world needs another software package for hosting run of the mill mining pools, as the existing ones are already pretty good. I’d really want to offer something truly unique before going the open source route, and I don’t think I’m there quite yet.

**RockSteady** — Do you have a Discord? What’s the best avenue for feedback?

**cryptonote.social** — Best places to reach me would be on Twitter [(https://twitter.com/CryptonoteSoci1)](https://twitter.com/CryptonoteSoci1) or through e-mail at [cryptonote.social@gmail.com](mailto:cryptonote.social@gmail.com). I don’t have my own Discord server but I’m easy to find on existing ones, as well as on Reddit.

**RockSteady** — Sounds good, I think that about covers it for our side, is there anything you’d like to add?

**cryptonote.social** — Don’t think so. It’s been fun!

**RockSteady** — Thanks!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/predictable-solo-mining-w-cryptonote-social-pool/)_._
