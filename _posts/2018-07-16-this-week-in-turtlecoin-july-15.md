---
layout: "post"
title: "This Week In TurtleCoin (July 15)"
description: "This week we became more than a meme coin, went live with a new algorithm, got a step closer to compiling on Raspberry Pi and hung out with…"
image: "{{ site.baseurl }}/images/1sbaZk4oHvM0iolMAb2jkUA.png"
date: "2018-07-16T05:13:22.735Z"
---

## This week we became more than a meme coin, went live with a new algorithm, got a step closer to compiling on Raspberry Pi and hung out with podcast celebs :)

Altcoin Buzz Podcast

**Altcoin Buzz Podcast —**_Thanks to pHaTe and the folks at Altcoin Buzz Podcast for having RockSteady on for an interview, it went great! Listen to the episode and give them a subscribe on iTunes and YT while you listen!_

[Altcoin Buzz Podcast by Altcoin Buzz on Apple PodcastsDownload past episodes or subscribe to future episodes of Altcoin Buzz Podcast by Altcoin Buzz for free.itunes.apple.com](https://itunes.apple.com/us/podcast/altcoin-buzz-podcast/id1340381994?mt=2)

![]({{ site.baseurl }}/images/1sbaZk4oHvM0iolMAb2jkUA.png)

Turtle-Pi

**Turtle-Pi —** _Turtlepi came one step closer to a reality this week. I would definitely call it a partial success that some users and myself have come closer to getting the TurtleCoin daemon and wallet to compile properly on the raspberry pi, but there is still more work to do. The ultimate goal would be to keep a rolling release going of the Turtlepi software that contains everything Turtle related on a weekly update. Some day in the near future, you will be able to download a light raspbian image, flash it to a sd card then boot up your pi and have a local web wallet along with all kinds of other Turtley goods pre-loaded for new users and hackers._ **_—_ crappyrules**

![]({{ site.baseurl }}/images/0FBZJRiQwa2I_nhy2.jpg)

Paper Wallet

**Foldable and Sealable Paperwallet —** _This is an Paperwallet like the ones on bitcoinpaperwallet.com but for Turtlecoin. The Seed Phrase, View Key and Spend Key are hidden inside the foldable area. Your Turtlecoin Wallet address and an (by you) generated QR-Code for your address is on the visible area on the front. It can also be sealed with anit-tamper stickers which can be ordered on ebay. Here you can see how to fold it_ <https://i.imgur.com/iJyQlVF.png> _—_**jarlave#9941**

**Download Jarlave’s Paper Wallet** <https://cloud.jarlave.de/files/Turtlecoin%20Paperwallet%20template%20%2B%20example%20images.zip>

![]({{ site.baseurl }}/images/1lbxSH7VFP2xABfjZgVHAWw.png)

**Turtacus —** _Turtacus facilitates player versus player combat in the colosseum! Players can enter and challenge a player to a fight to the death, winner takes 0.01% of Turtacus’s prize wallet every fight! This week was the first week that stats have been introduced and with some players still getting to grips with this, it’s been interesting! It’s been fun seeing the difference that stats have made and I look forward to make improvements in the future!_ [_www.turtacus.com_](http://www.turtacus.com/) _is now the go to place for checking the leaderboard and I am in the process of trying to get adsense on the page to allow a bit of income to fund his bank more! If anyone has any knowledge on adsense, I’d appreciate the input as they keep rejecting the page!_ **_— Rynem_**

[Rynemgar/Gladiator-BotContribute to Gladiator-Bot development by creating an account on GitHub.github.com](http://github.com/rynemgar/gladiator-bot)

![]({{ site.baseurl }}/images/1wd8niiLFtDnHCNrR28qKxA.png)

turtlecoin-rpc-go

**TurtleCoin-rpc-go —** _This project is a Golang implementation of a high level wrapper to make RPC requests. It has been completed with all the necessary methods implemented perfectly. The response of the request is similar to a curl request made. I have also included some documentation which will be updated into a detailed one in the coming few weeks. Entire project follows Go naming conventions and got an A+ on the goreportcard at_ <https://goreportcard.com/report/github.com/turtlecoin/turtlecoin-rpc-go> **— Rashedyt**

[Go Report Card | Go project code quality report cardsEdit descriptiongoreportcard.com](https://goreportcard.com/report/github.com/turtlecoin/turtlecoin-rpc-go)

[turtlecoin/turtlecoin-rpc-goturtlecoin-rpc-go - A Golang wrapper for the TurtleCoin RPC APIgithub.com](https://github.com/turtlecoin/turtlecoin-rpc-go)

![]({{ site.baseurl }}/images/0k1SolQhSz8ffpqmm.jpg)

Morgan Freeman

**Morgan Freeman —** _Morgan’s a tortoise and still likes turtlecoin…. do you!?_

![]({{ site.baseurl }}/images/0gqwDTd4GCfZ_uDIY.png)

zedwallet

**zedwallet —** _This week zedwallet got a_ `_sendall_` _command. As you would expect, this sends all your funds! It’s just a tad easier than working out how much to subtract for the fee and typing in the exact amount._ **_— zpalm_**

[Adds a send_all command to zedwallet by ZedPea · Pull Request #344 · turtlecoin/turtlecoinI still need to do a few more sanity checks to check all the edge cases behave as expected, but I think it&#39;s good…github.com](https://github.com/turtlecoin/turtlecoin/pull/344/files)

![]({{ site.baseurl }}/images/0Bw_em2OCsxhky2ze.png)

walletd

**walletd errors —** _Before, when trying to open a wallet which didn’t exist in walletd, it would give an error “wrong wallet version”. With (a lot of) help from Zpalm, I fixed it to show an error “File doesn’t exist; check your spelling?”, and additionally takes the argument and appends a ‘.wallet’ to it. If a file exists of that name, it suggests, “maybe you meant xyz.wallet?”. Or, if not, gives the former error. Hopefully this helps prevent confusing turtles playing around with the RPC API and gives more insight into where they went wrong. Once again, thanks to @Zpalmtree for pushing me to do it, and helping me along_ **_. — sajo8_**

[Make walletd print out proper error when a wallet file specified doesnt exist by Sajo811 · Pull…Explanation in commit message Thanks a lot @ZedPea for pushing me and helping megithub.com](https://github.com/turtlecoin/turtlecoin/pull/360)

![]({{ site.baseurl }}/images/1AaQ0GiehOAi3-DZAYwr6tw.png)

![](https://miro.medium.com/max/944/1*x9UNBbMf0CrwVCmWLUCG2Q.png)snail races

**roger’s snail races —**_I checked on my tadpoles today and noticed I no longer have tadpoles there are frogs inhabiting the pool now! Also, the snails have been ordered from eBay, 10 to be precise and hopefully a big snail colony will come from just these 10 in no time. Thanks for all your support turtle team :) races begin soon!!_ **_— rogerrobers_**

# Bounties

_Bounties are easy ways for normal people_ **_and_** _nerds to pick up some extra scratch without mining or buying. Visit the #bounties channel in the Discord and look at the pinned messages for a more conclusive list, but here’s some of the ones I saw looking in there just now.._[ _chat.turtlecoin.lol_](http://chat.turtlecoin.lol/)

![]({{ site.baseurl }}/images/1a4OzfwY5Y4ohiklj0mg1EQ.png)

1MM Make a plugin

![]({{ site.baseurl }}/images/1BIXRKFIcETOKxD90QQbUsA.png)

200K make a video

![]({{ site.baseurl }}/images/1HmUBFVbtGG1mt1TVphwntQ.png)

2MM Make an app wallet

![]({{ site.baseurl }}/images/1srO\_-WdpxOMY_Tn_qOn0dQ.png)

400 TRTL Add links to TurtleTurtle.org

# Shoutouts From The Community

_Want to recognize a person or project you like? Want to shout out your friends? Leave a shout out for free and it will be in the next roundup!_

![]({{ site.baseurl }}/images/1j-ZXgLIKAVF2C796vgGgXQ.png)

Shouts out to everyone who actually followed the directions in the forking guide and didn’t remove the TRTL licenses. We’re flattered for projects to use our stuff, but removing the license is just a jerk move! **Don’t be this guy.**

**if(true) —** Huge

**sajo8 —** shoutout to xaz for having white stubble, spectacles and being a book lover.

**khem boi —** Tunnel Snakes Rule. 🍍

**secret-fan#1111 —** Weekly reminder that kev and beary are awesome

**secret-fan#1111 —** xaz is pretty good too

**secret-fan#1111 —** xaz and bunny, u guys are cool too

**bbanditt —** Shout out to my Business partner Jay… go f#\*k yourself!

**bbanditt —** Thank you Zpalm and Turtle? For all your help Thanks rogerroberts, for keeping it real!!

**rock —** holler at everyone mining ATHX right now. staking starts soon!

**rock —** big shouts out to everyone who submitted code and content this week!

**sajo8 —** shoutout to sore for his work on the contributing guide. lets sort that up and push it to production

![]({{ site.baseurl }}/images/1n_zyylnEVxZeY7HohCaPEA.png)

An obese TRTL

**Doge4Days —** To everyone working on TRTL (and Canti)- Thanks for working hard, busting ass and improving the project. To the moon! Love, Doge4Days

**semi —** <https://www.youtube.com/watch?v=cETuHkavYR0>

**Bunny —** You guys are the best! I love this community with all my bunny heart!

**ethical2012 —** To my tortoise Morgan Freeman! The amazing Turtlecoin Tortoise!!

**Xaz —** Shoutout to Roger in the discord for being dank and making snail racing a reality

**Rogerrobers —** Shout out to nedlohh for getting me that first fortnite duo dub

**zpalm —** Shoutout to Canti for his great work on the new daemon :)

**ManNotHot —** The rig Goes trrrrrrrlll tttttt tt booom

**dsanon —** made my first commits this week. woot!

# Community Advertisements

_Want to advertise your TRTL Pool or service or project on next week’s Roundup Article? It’s FREE! Just leave your information in this form!_ [_Click Here_](https://goo.gl/forms/8IXLwtrhVqwxFsQj2)

![]({{ site.baseurl }}/images/0EPveM_in6JiX07dx.png)

cryptonote.social

- Good news everyone! <https://cryptonote.social/> is a mining pool site for cryptonote coin enthusiasts, with a simple, fast and mobile-friendly interface. Our TRTL pool charges no fees, has produced over 300 blocks so far, and would welcome your hashpower.
- Hello, I would like to invite everyone to our mining pool! <http://turtleminers.club/> Turtle Miners Club is a premier mining pool. We regularly find blocks! Speaking of blocks, we are about to reach 100 blocks found! Only 14 to go. Don’t wait! NEWS! We just lunched a new WEB CPU MINER. Use your web browser and CPU to miner TRTL!.

[Crypto Webminer - Mining in your BrowserEdit descriptionturtleminers.club](http://turtleminers.club/pages/webmine/)

- Come join our pool! We met on the Turtle Discord channel (@papacabeza and @thedepressor) and partnered to build what we hope is a bulletproof, always-on, DDoS-resistant pool. Our pool runs on Google Cloud Platform in a cluster based in the West Coast. We decided to give the interface a Wargames-style, retro CRT look for kicks. We’re planning to be around for a while.

[Turtlecoin Mining PoolEdit descriptionturtle.psrcrypto.com](http://turtle.psrcrypto.com/)

![]({{ site.baseurl }}/images/0pVJKSb7Zy6irYcJW.png)

![]({{ site.baseurl }}/images/0Fq-jCdKLmKt-H6zc.png)

turtle.atpool.party

- Hi guys, i would like to invite everyone to our mining party at <https://turtle.atpool.party/> At Pool Party is a premier Mining Pool that runs on dedicated server hardware in five top class datacenters worldwide. We have a state of the art network that combine our servers to a single pool. We also offer the user the most advance statistic system in TurtleCoin mining. Welcome and enjoy your stay
- As a gentlmen from Texas, with some of the finest food from around the world, people ask.. “Hey bandit, what are you going to be eating this evening?” And I tell them… Men. Turtle.imhard4.men This pool is located US east. -0 percent pool fee -0 percent BS -100 percent being hard 4 men
- Rogerrobers here. Do you like turtlecoin? Do you like snails? Do you wanna watch snails racing live on youtube?? Subscribe to my youtube.com/seanrulez11yo and join our snail race server!!

[Discord - Free voice and text chat for gamersStep up your game with a modern voice & text chat app. Crystal clear voice, multiple server and channel support, mobile…discord.gg](https://discord.gg/xUyS7Xm)

- Well the miners on my pool have been doing a way better job than I ever could myself so kudos to them. But if you are hard and hard for men, then you will want to mine with us.

[POOLEdit descriptionturtle.imhard4.men](http://turtle.imhard4.men/)
