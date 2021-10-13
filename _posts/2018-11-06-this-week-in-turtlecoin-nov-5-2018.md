---
layout: "post"
title: "This Week In TurtleCoin (Nov 5, 2018)"
description: "This week we all became game streamers on Twitch Turtle, and rode our time machines back to the 90’s to see what kind of websites we could build on a floppy! We’re on track to hit 13,000 users in the…"
image: "{{ site.baseurl }}/images/0HuX9IMBg6k0352UY.png"
date: "2018-11-06T05:59:31.780Z"
---

![]({{ site.baseurl }}/images/0HuX9IMBg6k0352UY.png)

This week we all became game streamers on Twitch Turtle, and rode our time machines back to the 90’s to see what kind of websites we could build on a floppy! We’re on track to hit 13,000 users in the Discord chat soon, join us! chat.turtlecoin.lol

# Developer Community Updates

**TwitchTurtle** — This week, I tried TwitchTurtle as a streamer. I played ARK Survival for the normal amount of time, and got a few thousand TRTL in tips (if youd like to join Tribe of Turtles, we’re on ragnarok pvp official 61). In all, it was a fun experience. Streamlabs makes it really easy with their own personal spin on OBS, a popular screencaster program we use to capture the screen. I was up and raining in about 6 or 7 minutes. One thing that’s cool is that DSAnon is adding in the messaging functionality for custom tip messages into Shellnet so you dont have to set up box turtle on your own to send a tip with a message via the blockchain. There’s room for improvement, but as a brand new integration, I’d be skeptical if there weren’t any wrinkles to smooth out. Watter has done a great job! Very fun! **— Rock**

[TwitchTurtleTwitchTurtle is a fast, simple, and secure Streamlabs donation servicetwitchturtle.com](https://twitchturtle.com/)

**TurtleCities** — I had been toying with the idea of making some type of user homepages for our regulars in the chat. I was inspired by webrings of homepages on sites like geocities, angelfire, and expages, those types of sites from the 90’s. While I didn’t build an entire frontend for WYSIWYG design, I did create a system that allows me to provision users manually who get a 1.44mb FTP account with no shell access, and a homepage url like <https://pages.turtlecoin.lol/~username.> The account gets created manually, and the user uses something like filezilla to connect via FTP and upload up to 1 floppy of web space. I suppose the next step is some type of shell account or BBS. I’d like to make it a paid service so you can get the page for free, and then upgrade to a dual density floppy or add shell access down the road. A lot of it is still up in the air waiting for someone to abuse it. I’d also like to automate account creation, as I’m currently using a google form and webmin. What’s cool is that I built a Bash script that generates the main page every 30 seconds server side and updates a list with a bunch of system specs and links to the latest modified pages. **— Rock**

[turtlecoin/pages.turtlecoin.lolturtlecities. Contribute to turtlecoin/pages.turtlecoin.lol development by creating an account on GitHub.github.com](https://github.com/turtlecoin/pages.turtlecoin.lol)

[TurtleCities™Edit descriptionpages.turtlecoin.lol](http://pages.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0jC6ookUAAelksuLd.png)

**Swanson Clicker** — Now introducing Swanson Clicker! Get addicted to a Clicker Game all over again…Turtle style! Complete with 3 different upgrades and more features to come. **— xaz**

[Swanson ClickerEdit descriptionswansonclicker.com](http://swansonclicker.com/)

**TurtlePay™** — I’ve been working the last few weeks hopping between core development and TurtlePay™. Most of my time there has been spent formulating plans including design documents that are in the repo. As always, slow and steady is the name of the game. I’ve published a draft development roadmap for everyone to take a look at. Feel free to ask questions, provide feedback, or help out. TurtlePay™ will hopefully build on the foundation of a lot of the tools I’ve already published. It’s like fitting together a bunch of puzzle pieces that we didn’t even realize were puzzle pieces :) It’s definitely an exciting project and I’m looking forward to what others can build based upon the services the project will offer. **— IBurnMyCD**

[TurtlePay™TurtlePay™: Fun, Fast, & Easy Crypto Payments. TurtlePay™ has 2 repositories available. Follow their code on GitHub.github.com](https://github.com/turtlepay)

![]({{ site.baseurl }}/images/0UbjqlmGHJHDbtXqN.png)

**TwitchTurtle** — TwitchTurtle is a fast, simple, and secure way to donate to twitch streamers. Over the past weeks, there have been many improvements, such as a docs site at <https://docs.twitchturtle.com/> and many improvements to the web dashboard. Adding messages have never been easier with the new Shellnet integration, you can see more at the docs site. Thank you to everyone helping this project live and grow! **— Watt3r**

[TwitchTurtleTwitchTurtle is a fast, simple, and secure Streamlabs donation servicetwitchturtle.com](https://twitchturtle.com/)

![]({{ site.baseurl }}/images/0FROJgkCH6R23G6JS.jpg)

**Krang —** Been too busy with work and social the last few weeks. Doing nothing worth mentioning apart from starting mining some Soft-Shell coins and that is looking good, love a good solo mine with no pools, Cant wait to unleash that into the TRTL network. Today I’m working on adding more customization in Terraform and getting back into the groove of things, probably take a look at turtle.services and ibmcd node.js automation. Getting Schwifty. **— Slash-atello**

[4Reallive/krangThe TurtleCoin Blockchain Automation Suite. Contribute to 4Reallive/krang development by creating an account on GitHub.github.com](https://github.com/4Reallive/krang/tree/Development)

![]({{ site.baseurl }}/images/0u3mRCvTgNZevFRmH.png)

**Walletgreen / turtle-service rewrite —** Good progress this week on the rewrite. I got fusion transactions working, which are essentially a standard transaction, but they have a few rules required to allow them to be zero fee. With some help from iburnmycd I implemented a nice algorithm, which should be able to pick the best inputs to optimize together. Pretty much everything on the backend is complete, minus some rare crashes which I’m still debugging :( I started rewriting zedwallet using the new backend, to help me figure out where stuff is broken or could do with a rework. So far, it’s nearly complete, and has helped me find nearly all the bugs. \*Hopefully\* we will see it being used in a release after not too long. Since the wallet no longer uses some hacky dispatcher stuff, we can freely do everything on separate threads. With the current implementation, you have to update the wallet sync progress only on the main thread. To work around this, current zedwallet has a pretty ugly method, where it launches a thread to wait for input, and refreshes in the background whilst no input is coming, which is hard to follow, and not very performant. With the rewrite, we just attach to the event handler, and print out the transactions as they come to us, with a simple flag to ensure we’re not printing in the middle of a command, like transferring. Once everything is polished, this will hopefully make it a lot more trivial to add new features to wallets, with a sane, readable backend. I’d love to see some more core contributors — C++ isn’t that scary when you get into it! Oh, forget to mention — scan height works a lot better now — instead of starting at zero, and scanning the blocks below the height ‘quickly’ — it just skips those blocks, and starts right at the height you want to scan from. Still haven’t got around to writing that article on how transactions work… **— zpalm**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/tree/walletgreen-rewrite)

**TurtleStash** — WhassupZA has really been championing this project. Currently there’s a few kinks to work out, but you can create wallets with seeds and read transactions as they come in, but there’s a weird timeout issue when you try to send them. This should work itself out soon, and it’s really cool to see the progress. Plenteum and Masari team have done the entire project conversion for TRTL and it’s been great watching things come together. Just a reminder, TurtleStash is a website running the clientless web wallet forked from Masari. This is important because it is a webwallet that allows the user to own their own keys and not depend on a third party to run the software. **— rock**

[turtlecoin/turtlecoin-webwallet-jsTurtleCoin Clientside Web Wallet. Contribute to turtlecoin/turtlecoin-webwallet-js development by creating an account…github.com](http://github.com/turtlecoin/turtlecoin-webwallet-js)

# Community Bounties

**10,000 TRTL —** create a Rastafari emoji and or graphical art **— GiGaUrtle**

**20,000 TRTL** — TRTL Meme that shows TRTL as the main currency in the future **— wichtigwicht 🇩🇪**

**75,000 TRTL —** I need a quick site done up with a simple (very simple) shopping cart interface that does the following: 1) guest selects “purchase access” 2) guest is given an address and payment ID to send the amount of TRTL to 3) once TRTL is received, guest is granted the ability to download a file up to 5 times. 4) upon limit reached, access to file is denied. Bonus bounty: +25K TRTL if TRTL.Services is used. Project will be used to host a TRTL blockchain bootstrap. **— IBurnMyCd**

# Fork Watch!

![]({{ site.baseurl }}/images/0cXJkO4By7U5s0bOD.jpg)

**Name of your TRTL fork:** GrubMine

**Github link for your code:** <https://github.com/Franzferdinan51/GrubMine>

**What is special or new about your network?**

To help us spread knowledge and understanding of blockchain technology via our diverse products

# Community Advertising

- High Availability, stupid friendly, and cheap mining pools. Hosted in the middle of ‘Murica so you can expect the most excellent of pings from anywhere in the US. We also have a active vibrant discord community, who is quick to answer any questions you have. So jump off that mega pool and join something smaller, and something with Llamas. I’m Mr. Horse and I approve this message. Paid for my Mr. Horse for Congress. [http://trtl.llama.horse](http://trtl.llama.horse/)
- play a quick game o’ skribbl <https://skribbl.io/?rOlUyY6dxv>
- 0 fee public nodes: greywolf Germany @ turtlenode.co:11898 & greywolf London @ turtlenode.me:11898

# Shoutouts & Thanks

rogerrobers — Shout out billiontrtlhomepage.lima-city.de

ChiefCoin — Shoutout for all Twitter Turtles spreading Turtle Love out there ✌

greywolf³˜ — thanks to labaylabay for the reach-out … a good role model for [https://medium.com/@turtlecoin/how-to-be-a-good-turtle-20a427028a18](http://blog.turtlecoin.lol/@turtlecoin/how-to-be-a-good-turtle-20a427028a18)

. — I remember you canti 😘

@Knomore — Llama.Horse — Shout out to the devs for this update that removed old outdated nodes from the network. I feels like our nodes are having less issues and connect to less garbage peers now. Sweet hookup fellas!

Rogerrobers — Shout out to pages.turtlecoin.lol !! Thanks rock :)

greywolf³˜ — thanks to iburnmycd for the TurtleCoin-HA update, nodes are running fine now

JerMeeeeeeee — Shout out to the soft shell crew, get those CPUs cooking!!!

JerMe404 — Thanks AFDI for keeping everyone going while discord image upload was broken!

Slash-atello — SHOUTS to wichtigwicht 🇩🇪 who started running meme competitions. It’s hard to manage that along with everything else, although it is sorely needed. Encourage everyone not coding to give it a shot. Your chance to shape the community.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-nov-5-2018/)_._
