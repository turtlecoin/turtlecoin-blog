---
layout: "post"
title: "This Week in TurtleCoin (July 9, 2018)"
description: "This week we opened our school of shitcoin artistry, added about 10 devs to the fold, and forgot to write about it until Monday. Hard work…"
image: "{{ site.baseurl }}/images/09SKIXM43hh5TwBU8.jpg"
date: "2018-07-10T01:03:27.433Z"
---

## This week we opened our school of shitcoin artistry, added about 10 devs to the fold, and forgot to write about it until Monday. Hard work over here, folks. Don’t get none on ya! Check it out!

![]({{ site.baseurl }}/images/0jj7FZDKUTOWE5s44.png)

Would you be interested in one artisinal shitcoin network?

**Zpalmtree’s “_How To Fork TurtleCoin”_ Tutorial —** “_I had a really fun time this weekend live-blogging the process of making my own altcoin forked from TurtleCoin with Zpalmtree’s new guide for how to fork TurtleCoin properly._

_A lot of aspiring devs were forking TurtleCoin and afraid to ask for help or making rookie mistakes like removing licenses from the source code, so we decided to help the community by making a step by step guide with all of the parameters laid out with notes and details. Making an altcoin can be frustrating for some and we want to make it easier for others to have the same chances we had when making a new network._

_Check out my article about the whole process, and mine a few blocks of “Athena” my new slow settlement-layer blockchain with 1 hour blocks! I’m thinking I might keep this one around for later just in case.._” — RockSteady

[How To Fork Turtle Cointurtlecoin - TurtleCoin is a private, fast, and easy way to send money to friends and businesses!github.com](https://github.com/turtlecoin/turtlecoin/wiki/Forking-Turtlecoin)

[Altcoin 101 — Create a Cryptonote Privacy Coin Clone in One HourToday we’re following a howto guide for making your own privacy coin network, fast and easy!medium.com](https://medium.com/@turtlecoin/altcoin-101-create-a-cryptonote-privacy-coin-clone-in-one-hour-f14bff7eb2fd)

[athena-network/athenaathena - Athena is a slow block settlement layer for other blockchainsgithub.com](https://github.com/athena-network/athena)

![]({{ site.baseurl }}/images/01gFrsS3CoRdtyFTf.png)

Integrated Addresses!

**Integrated Addresses —** “_This week I’ve added integrated addresses to both walletd and zedwallet. (Coming to your favourite GUI soon™) You can start using them now if you build from source, or wait for 0.6.4…_
_You might be wondering what an integrated address is. In short, it’s a standard TRTL address, and a payment ID squished together. Here I’m using it to send to my tipjar without providing a payment ID:_ <https://i.imgur.com/pJQFbGX.png> _\[That’s a big address, for you\]_
_Why is this handy? Well, it means an exchange, or other service which requires payment ID’s to transact can simply send you an integrated address instead of an address and payment ID pair. This integrated address is then parsed by your wallet into an address and payment ID pair internally, and sent as a normal transaction. This means you no longer have to worry about using the wrong payment ID or forgetting it. If you’ve used Monero derived coins, then you might have used one before. Monero’s block template allows 16 char payment IDs, so their integrated addresses are a lot shorter, at about 115 characters. TurtleCoin integrated addresses are a whopping 236 characters! If you’re an RPC API maintainer, you might want to consider adding the createIntegratedAddress() method to your API so users can easily create integrated addresses to supply to people — more info here:_ <https://github.com/turtlecoin/turtlecoin/pull/337> _Right now there’s not really anything supporting integrated addresses, but hopefully soon exchanges and other services will adopt them. The tipjar could support them too! You can manually create integrated addresses in zedwallet to mess around with by using the_ `_makeintegratedaddress_` _command._” **— Zpalmtree**

[Add integrated addresses to walletd by ZedPea · Pull Request #337 · turtlecoin/turtlecoinAdds integrated address support to walletd. Adds a new RPC call, createIntegratedAddress(), that takes a parameter…github.com](https://github.com/turtlecoin/turtlecoin/pull/337)

[Just curious about mining vs minting here..Vote Now! \[proof of work\] \[proof of stake\] \[im just a turtle, shrug\]www.strawpoll.me](https://www.strawpoll.me/16050814)

![]({{ site.baseurl }}/images/1nocTr9RrJZzmf7jT9aSQGw.png)

Turtacus

**Gladiator Bot (Turtacus) —** “_Turtacus operates in the colosseum providing members with a player versus player combat experience. Last week I mentioned that stats were in the making and were causing me problems and headaches. This week… Stats went live! This now means that every players level was reset to Level 1 and experience is now a climbing difficulty. For every level a player earns, they can now purchase a maximum of 3 stat points. These stats can be assigned to strength (to increase your attack power), defense (to reduce incoming damage) or agility (to mildly increase your chances of hitting your opponent). This is all completely custom. You can assign your points however you please making combat a truly dynamic experience! Obviously over the coming weeks, there will be changes that need to be made as stats develop. It could be that limits on the difference between player stats in combat need to be added so that people aren’t getting one shotted, it could be that the bonus added by stats needs increasing or decreasing. For now, stats are in! Previously, experience was awarded at 20xp per win with 5 wins being required to level up, no matter the level. This now works on a sliding scale — 50xp required to reach level 2, 100xp for level 3, 150xp for level 4 etc etc. This means the higher your level, the more you have to win to level up again. BUT — You no longer get 20xp per fight unless the person your fighting has an identical amount of used stat points. Experience is now worked out in the following manner: (loser strength+defense+agility minus winner strength+denfense+agility) + 20\. If the above equation works out to less than 5xp, the player will be awarded 5xp. otherwise, you will get the amount it works out to. So, beat a player with higher stats than you and you’ll be awarded in kind! Stats are all viewable on the new and improved_ [_http://www.turtacus.com_](http://www.turtacus.com/) _website! I look forward to seeing how stats effects the game in the coming days and appreciate any feedback given._” **Rynem**

[Rynemgar/Gladiator-BotContribute to Gladiator-Bot development by creating an account on GitHub.www.github.com](https://www.github.com/rynemgar/gladiator-bot)

[TurtacusWebsiteEdit descriptionwww.turtacus.com](http://www.turtacus.com/)

![]({{ site.baseurl }}/images/09SKIXM43hh5TwBU8.jpg)

TFW you mine your first solo block in weeks

# Community Advertisements

_Want to advertise your TRTL Pool or service or project on next week’s Roundup Article? It’s FREE! Just leave your information in this form!_ [_Click Here_](https://goo.gl/forms/8IXLwtrhVqwxFsQj2)

- Bounty! 50k turtle bounty for obeese looking Turtle emoji!  
  \-submissions to bounties room or @bbanditt  
  \-square, png format prefered  
  \-deadline July 13th 2018
- Turtle Miners Club is a premier mining pool for anyone wanting to mine! We are small, but steadily growing. Everyone is welcome to join! NEWS: We just released a new website featuring Web CPU Mining. Join the club now at

[Cryptonote Mining PoolEdit descriptionturtleminers.club](http://turtleminers.club/)

- Come and join us mining down in Mordor at in the NZ/AU TRTL pool at <https://trtl.heigh-ho.funkypenguin.co.nz/> — Small pool, low fees, responsive admin, discord for support!

[Funky Penguin's NZ TRTL Mining PoolEdit descriptiontrtl.heigh-ho.funkypenguin.co.nz](https://trtl.heigh-ho.funkypenguin.co.nz/)

# Shoutouts From The Community

_Want to recognize a person or project you like? Want to shout out your friends? Leave a shout out for free and it will be in the next roundup!_

**secret-fan#1111** — shoutout to kev and bearybullish for being awesome

**Sajo8#2953 —** Shout out to gt3000 for helping me with the game dev

**Sajo8#2953 —** shoutout to zpalm for helping me code

🍍**ANON**🍍 **—** shoutout pineapple crew, behind the bleachers after TRTL class

**Khem Boi —** Shout out to all the members in this community for making all of this a reality.

**Khem Boi —** Shout out to beary bullish making my suspicious bear emoji a reality lmao

**CIAGUY69 —** Hey Extra! Nice penis man!

**funkypenguin —** Thank you to any generous turtles who [supported my geek cookbook](https://www.patreon.com/funkypenguin) after reading the[ detailed guide on establishing a TRTL mining pool under docker](https://geek-cookbook.funkypenguin.co.nz/recipies/turtle-pool/)

**anon —** shoutout worktips for doing the right thing

**ANON —** Happy Birthday Alien

**tjwmagic —** Shout out to thescimitarr for deploying a new Web CPU Miner for our pool! I invite everyone to check it out at h[ttp://turtleminers.club/pages/webmine/](http://turtleminers.club/pages/webmine/) !

**Rogerrobers —** Shout out to bbanditt, jerme, and alien for always spreading the TurtleCoin love and being so generous to our discord members

**ATHENAFAN1 —** Mining athena with 2 ryzen and vegas on turtle

**Rock —** Shouts out to Canti, IBMCD, Zpalmtree, Soregums, Aiwe, Nichop, Jagerman, cntemple, imperdin, LeTurt, systemdot96, RashedYT, Desp, Jon and everyone who joined or contributed to core dev this week. You’re all a big inspiration to me, and I’m happy to share this experience with you.

**Rock —** I would like to recognize RashedYT who’s made some big steps toward learning Golang, and I’m very proud watching his progress!

**Rock —** Thank you to -Serena- from Dero community for coming to us to apologize, I hope to put this behind us and move forward as a community together.

**Rock —** Karai whitepaper soon. Want to help co-author it? Ping me in the #dev_karai channel and let’s work this together

![]({{ site.baseurl }}/images/1xeCO4lFobhNODO_7Cqaw0g.png)

gotcha 🍍
