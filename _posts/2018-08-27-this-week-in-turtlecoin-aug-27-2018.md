---
layout: "post"
title: "This Week In TurtleCoin (AUG 27, 2018)"
description: "TRTL CLI — TRTL CLI is a tool to check TurtleCoin’s network status and straight from your terminal. Right now you can check the latest price, networks hashrate, calculate your TRTL net worth or print…"
image: "{{ site.baseurl }}/images/1CpTnwnKR3wq1I23dNEEt4g.jpeg"
date: "2018-08-27T23:03:53.892Z"
---

![]({{ site.baseurl }}/images/1CpTnwnKR3wq1I23dNEEt4g.jpeg)

Browns1964Champs made this :D

# Development Updates

TRTL CLI — TRTL CLI is a tool to check TurtleCoin’s network status and straight from your terminal. Right now you can check the latest price, networks hashrate, calculate your TRTL net worth or print a swanson with \`\`\`trtl ascii swanson\`\`\` thanks to Xaz’s contributions. Feel free to add new things and I will merge it right away, the code is really simple. — mrrovot

<https://github.com/mrrovot/trtl-cli>

[mrrovot/trtl-cliTRTL network status command line interface. Contribute to mrrovot/trtl-cli development by creating an account on…github.com](https://github.com/mrrovot/trtl-cli)

The Turtle Squad — The Turtle Street Team Is finally here! This is your chance to score some sweet Turtle swag, while spreading the good word of Turtlecoin. The street team is a project that aims to spread interest and awareness world wide to Turtlecoin. Learn more and apply via the Turtle Squad street team portal! — bbanditt

[https://turtlestreet.team](https://turtlestreet.team/)

[Turtle Squad - TurtleCoin Street TeamThanks for visiting the site Turtles! The TurtleCoin Street Team is a project that aims to spread awareness of our…turtlestreet.team](https://turtlestreet.team/)

Gotta scan fast — You might have wondered when you create a new wallet — why the heck am I scanning all the blocks from earlier that don’t contain my transactions?! Or perhaps you would have liked to be able to import your wallet keys from a certain height, knowing when you created it.

Well, this functionality has now been added to zedwallet and turtle-service. When creating a wallet, no blocks will be scanned until it gets to the time of the creation. And when importing a wallet, it will prompt you for the height you created the wallet at, to only start scanning when it gets to that height.

Hopefully this feature will be added to the GUI wallets soon, so everyone can enjoy it.

One thing to note is that you do still have to download the hashes of the blocks before the start of scanning, so it’s not \*instant\*. It is, however, MUCH faster. From my tests, it took about 7 minutes to download the first 500,000 blocks, not scanning any of them. This was using a public node, so I imagine it will be much faster on a remote node.

Coming soon™ to a release near you — Zpalm

<https://github.com/turtlecoin/turtlecoin/pull/443>

[\[ENHANCEMENT\] Allow scanning from a specific height when importing a wallet by ZedPea · Pull…Adds support to both turtle-service and zedwallet for starting the wallet scanning at a specific height when importing…github.com](https://github.com/turtlecoin/turtlecoin/pull/443)

TurtlePi — Huge steps were made this week advancing our cause to bring TurtleCoin to the Raspberry Pi and ARM devices. Quite a few very appreciated man hours were invested making this a closer reality. Over the next week I am hoping to have a small image prepared for download that will include a web wallet and the ability to run a full daemon on the PI with a minimal 64 bit raspbian image. The long term goal is to load the disk image will all things Turtle and also a desktop so new users can download and burn the image to an sd card, boot up and begin their trip down the Turtle hole. — crappyrules

<https://github.com/turtlecoin/turtlecoin>

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin)

TurtleCoin on the Raspberry Pi — This week we got TurtleCoin compiling on the Raspberry Pi 3b+. Thanks to everyone who helped with this.

It works great, and I’m currently running a TurtleCoind node and zedwallet on it, so I can ssh in and and it’s all ready and up to date for me to use.

To speak to the motivations behind getting TurtleCoin on a Pi, I’ll quote RockSteady:

_“Efforts we like to focus on are educational in nature, for example our project “box-turtle” seeks to make easy to deploy raspberry pis with turtle wallets embedded in them for us to use when sponsoring hackathons for youngsters. This project has web elements as well as system coding elements, and even graphics if someone were so inclined, so it’s a great opportunity to get funding from businesses to supply those materials and spaces for us to engage with the community._
_It would be a great help to find sponsors for a few hundred raspberry pi 3b+’s, and finding hackathon groups preferably in areas with a concentration of Turtles where we can engage with youngsters and teach them a bit about how this stuff works. Our core mission is bridging the gap between those in the know, and those who are not. We would like to cultivate a future culture that embraces blockchain as well as development as a whole, so that when laws are made concerning our industry in the coming years, they’ll be informed decisions, rather than fearful acts of legislation.”_

There was a a 2.3 million TRTL bounty for achieving this, and it was pretty trivial to do, actually. So, if you’re a decent programmer, check out the bounties for a great way to earn some TRTL :) Thanks to Jerme for the decal ;) -Zpalm

<https://github.com/turtlecoin/meta/issues/118>

[EXPEDITION ARM · Issue #118 · turtlecoin/metaGIVE THIS TURTLE SOME ARMgithub.com](https://github.com/turtlecoin/meta/issues/118)

TurtleCoin ARM For Raspberry Pi 3 B+ — The three of us recently completed the bounty as listed under the meta repo and the #bounties channel which listed a total bounty of 2,600,000 TRTL. It took many long hours of work but in the end the effort was worth it as now we have an ARM build that works great on Raspberry Pi 3 B+ — IBurnMyCd, zpalmtree, rashedmyt

<https://github.com/turtlecoin/meta/issues/118>

[EXPEDITION ARM · Issue #118 · turtlecoin/metaGIVE THIS TURTLE SOME ARMgithub.com](https://github.com/turtlecoin/meta/issues/118)

- Turtlecoin subreddit posts on Twitter. [www.twitter.com/RedditTrtl](http://www.twitter.com/RedditTrtl)  
  Posts new posts from r/TRTL to twitter please give it a follow.

![]({{ site.baseurl }}/images/0VkUZy4mYTC7uzYD\_.png)

- The TurtleCoin Street Team is Here! Welcome to the Turtlecoin Street Team! Here is your chance to score some sweet Swag while shilling the good word of Turtle. Please see the Street Team Portal for more information. [https://turtlestreet.team](https://turtlestreet.team/)

![]({{ site.baseurl }}/images/0LJHmMZj1ldCpB1Ef.png)

- Mine2Gether invites you to our weekly Blockchain Bingo!  
  The next Blockchain Bingo is September 3rd @ 5 PM GMT, in our discord #bingo channel: <https://discordapp.com/invite/AT3AAxV>  
  Blockchain bingo is for community fun, open to everyone, and completely free to play!  
  It is a variation and similar to traditional bingo, and uses the turtle blockchain to draw the numbers: <https://trtl.mine2gether.com/#bingo>  
  Everyone is welcome! 50K TRTL prizes, 250K jackpot, slots mini game, and more! Hope to see you there!
- Do you wanna play fantasy football? Have you always wanted to play with trtl up for grabs instead of being forced to eat cat food? Well have I got the thing for you! TurtleCoin fantasy football is looking for more members to join us as we combine fantasy football and crypto! Our discord server is <https://discord.gg/SxpKNUn> and we will be using the sleeper app/website to play! For more info talk to me Rogerrobers or @Browns1964Champs t_smile anyone can join the server just to watch it unfold, the more the merrier I say
- <https://turtlenode.net/> public.turtlenode.net:11898 European based node services geo located
- Everyone mining Turtlecoin, I invite you to join our small pool and help decentralize the network. Even your small hashrate would help the TurtleCoin network to spread and stabilize. Our pool is stable and has found around 450 blocks over the course of 3 months. Please consider joining our pool <https://turtleminers.club/>

# Community Shoutouts

mrrovot — A shoutout to xaz and Z for helping me out with TRTL cli

mkid — “I have 4 asic rigs mining this coin and getting over 25 million a day, no one person should every be able to mine so many of any coin in 1 day”

bbanditt — Shout out to Crappy for not dieing!

crappyrules — Huge thumbs up to cison for being an amazing and turtley turtlecoiner. He runs the best damn pools and services! TurtleCoin’s most prized asset, is a sweede!

greywolf — Thanks to zerouan for spending much time helping me try to figure out an odd GPU error. Between Mufalo and AFDI, how can anyone not be smiling?

Alien — Shout out to the OGs Turtle? and Zpalm for being a part of the Turtle world.

Rogerrobers — Shout out to snail races, mufalo is still undefeated! Will the streak continue this week?

greywolf — #(if not too late, I forgot 1) Thanks to Roger Robers for taking the time and energy to put together the snail races.

thescimitarr — A big shoutout to Zedpea for implementing the scanning wallet feature from a specific height.

thescimitarr — Discotim and Zedpea for implementing pool-guardian

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-aug-27-2018/)_._
