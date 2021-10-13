---
layout: "post"
title: "This Week in TurtleCoin (April 15, 2019)"
description: "Coming in hot with the dual issue! This Week and Last Week in TurtleCoin just didn’t have the same ring to it, so we did our best with the title. As you know this is a semi weekly article we like to…"
image: "{{ site.baseurl }}/images/0q4Dp7ojTcQwH7M3l.gif"
date: "2019-04-16T05:38:10.941Z"
---

![]({{ site.baseurl }}/images/0q4Dp7ojTcQwH7M3l.gif)

Coming in hot with the dual issue! This Week and Last Week in TurtleCoin just didn’t have the same ring to it, so we did our best with the title. As you know this is a semi weekly article we like to do when time permits to keep the community up to date with our progress. If this is your first time with us, stop by the chat and say hello :-)

**Join TurtleCoin Discord @** [**chat.turtlecoin.lol**](http://chat.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0vgHouKmZxZcmJVM4.gif)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

**_To submit your update, click this exceedingly long link_** <https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform>

![]({{ site.baseurl }}/images/0pkaP-fnS8XaJjPUv.png)

**Turtle Express Starter**

A boiler template for node.js using express.js for quick development. Comes with user system, dashboard and settings, including 2FA and password management. Further comes with a few small middleware scripts for RabbitMQ, user/input validation and recapcha and 2FA verification. It uses knex.js for sql query building and supports mysql, postgres, sqlite, and oracle. knex.js also builds your database schema for your, see the schema.js file in /utils/db. **fexra**

[fexra/turtle-express-starterBoiler template for node.js using express.js and a bunch of other goodies. - fexra/turtle-express-startergithub.com](https://github.com/fexra/turtle-express-starter)

> The current global hashrate is **254.57 MH/s**
>
> It’s probably gang-related.

![]({{ site.baseurl }}/images/0TjzuMP6S97_e1AK1.png)

**TRTL Button**

Hi Turtles! Super excited to share TRTL Button this week, you can generate a button for free and start accepting TRTL with just 2 lines of code on any webpage, it is powered by TurtlePay behind the scenes and it is super simple to setup, just a few clicks.

_I am also offering a bounty of 100TRTL for anyone who adds a ‘Pay With TRTL’ button to a web page! (check bounty section)_

You can test a live site using the button (check the source to see how it works) here [https://trtlbutton.surge.sh](https://trtlbutton.surge.sh/)Please try it out and let me know if you find any bugs or have feedback.” **Turtle Max**

[TurtleCoin Button WidgetAdvantages over showing your wallet and ask for payments: the end user can see a live loader of the status of the…trtlbutton.com](https://trtlbutton.com/)

![]({{ site.baseurl }}/images/0CLeo0afPUyMRbhAU.png)

**TRTLint**

TRTLint provides a free API to convert a TurtleCoin address and a payment ID to an integrated address. The HTTP API is easy and free to use. It’s free for projects and of course for commercial use too. If you find the service helpful, please consider a donation at <https://trtlint.de.cool/#donate> **fipsi | The Machine**

![]({{ site.baseurl }}/images/0qu8YQCn_lidpGX2e)

**Boostrap’s Back Baby**

“I had been watching an influx of new users coming into the discord lately asking why it takes so long to sync, there are a few options to use. public node, checkpoints or just wait, wait, wait……..

So I thought why not bring back the trusty ol bootsrap for those who want to run their own daemon, so I zipped up my DB and trtl.se was born. I have rented 2 seedboxes with unlimited bandwidth, 1 with a 20 Gbit/s connection and 1 with a 1.5Gbit connection. The theory was to release it as torrent only however I feel the need for a direct download is also required for ease of use so have put that on the site to see how it goes.

I plan to add some tutorials on the site on how and where to put the downloaded files and also make the site a little bit better and smaller css wise.

A shoutout to TurtlePay and TurtleButton for the awesome work on providing an easy donate link for those who like to donate to these kind of projects.  
If you find the bootstrap useful and it is something that we need, give me a shoutout and I will make sure it’s updated once a month and keep the seedboxes running.” **aneki**

[TurtleCoin Bootstrap©2019 TurtleCoin Bootstrap powered by TurtlePay™. and TurtleButton™.trtl.se](https://trtl.se/)

![Image result for money turtle](https://miro.medium.com/max/60/0*d5RgNtKueYe34w43.JPG?q=20)

![Image result for money turtle](https://miro.medium.com/max/902/0*d5RgNtKueYe34w43.JPG)

**TurtlePay**

Over the last week or so, with the help of @Turtle Max#3183, we’ve added the ability to generate a payment request, encrypt it, and use it later to start the payment process. @Turtle Max#3183 has leveraged this to create <https://trtlbutton.com/> which makes it very easy to add a simple “pay now” style button to any site. The button leverages TurtlePay to handle transaction processing and we’ve found it in use in the wild in a few different ways. We’re excited to see what else the community can build using the base things we’ve put together. If you have any ideas or suggestions, please don’t hesitate to swing by #dev_turtlepay to let everyone know. **IBMCD**

[TurtlePayTurtleCoin payments processing for developers, by developers.turtlepay.io](https://turtlepay.io/)

![Image result for hot bikini](https://miro.medium.com/max/60/0*CIsZindQaB8ylaRF?q=20)

![Image result for hot bikini](https://miro.medium.com/max/1400/0*CIsZindQaB8ylaRF)

I know this pic has nothing to do with the next post, but the post didn’t have a picture attached and I really wanted you to not miss it. Congratulations, you played yourself. **Buzzfeed taught me this.**

**TurtleCoin**

For those of you watching #dev_general, you’ve probably seen the notices from the GitHub bot that @zpalmtree#1337 and myself are trying to clean up some of the open issues on the repo by submitting patches. These patches resolve a few open issues as well as add new functionality to the core suite of tools.

One of the new sets of features I’m really excited about are those added via: <https://github.com/turtlecoin/turtlecoin/pull/769.> Most notably the new — rewind argument that will hopefully allow people to recover from local DB corruption without a full re-synchronization of the blockchain.

\* Builds & Links \[sqlite3\](https://www.sqlite.org/index.html) into the project  
\* \*\*Experimental:\*\* Enables the use of of a sqlite3 database for the local blockchain cache in the daemon via the \` — sqlite\` command line argument (replaces \`blocks.bin\` and \`blockindexes.bin\` with \`blocks.bin.sqlite3\`)  
\* Conversion between the two formats is \*\*not\*\* currently supported. Switching between the two mechanisms will require a \*\*full re-synchronization\*\* of the local copy of the blockchain  
\* Adds the command line argument \` — resync\` to the daemon that deletes all of the relevant data from the data directory which is useful for forcing a resync without having to look for the data directory on the different platforms  
\* Adds the command line argument \` — rewind #\` to the daemon whereby it will \[rewind\](https://en.wikipedia.org/wiki/Be\_Kind\_Rewind) the local blockchain cache to a point where the blockchain syncronization will \*\*restart\*\* at the specified block (inclusive).  
\* This is useful in attempting to \*recover from arbitrary database corruption\* (see #694 and countless Discord discussions in almost every channel) as it removes blockchain data starting from the specified height  
\* Altered the core “Corrupted Blockchain Database” message to provide possible recovery solutions including using the \` — rewind #\` and \` — resync\` options  
\* Altered the daemon to always create the directory specified by \` — data-dir\` if it doesn’t exist thereby preventing the dreaded message about the directory not existing. **IBMCD**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin)

![]({{ site.baseurl }}/images/0vTPJTV5wyA2GuUwa)

![]({{ site.baseurl }}/images/0Ht7kIhOb0-fg9HlK)

**TurtlePay & TurtleCoin**

I’ve been working on some concept artwork and assets for a few different marketing items to be used when advertising that TurtleCoin is accepted in by a merchant/vendor. I had a bunch of drink coasters, window clings, and tent cards printed up recently to see how they look. I’ve been leaving a handful of the coasters around London while I’m in the area and will be leaving some of all of them with @zpalmtree#1337 when I meet up with him later this week. He’s promised to guerrilla market using the window clings — let’s see how this goes. **IBMCD**

![Image result for dora the explorer turtle](https://miro.medium.com/max/60/0*7pbp8-Ev5PhwtfTV?q=20)

![Image result for dora the explorer turtle](https://miro.medium.com/max/1400/0*7pbp8-Ev5PhwtfTV)

**Turtle Explorer Desktop (Local Turtle Explorer)**

This is just an GUI update based on the previous version. The new version uses kivy instead of pyQt5\. I decided to use kivy just so to explore different tools for python. Also a more clear overview of the program is added in the README.md in the github repo. **Sabo (Revolutionary)**

[turtlecoin/turtle-explorer-desktopContribute to turtlecoin/turtle-explorer-desktop development by creating an account on GitHub.github.com](https://github.com/turtlecoin/turtle-explorer-desktop/tree/master)

![]({{ site.baseurl }}/images/0yX_KYImJzFNQQIcV.png)

**TonChan + wallet-api**

TonChan v0.1.0 went out a while back, with some features I talked about in a previous roundup, I think. The main fix was swapping the database backend. The stats are looking great, with app crashes WAY down. Have basically had no bugs reported, so this is looking like the first app release which is working pretty perfectly. Hopefully your experience is similar.

_I’m noticing quite a few crashes still being reported from people running v0.0.8 — please upgrade! Less crashes and more features :)_

On another note, I was working on some performance improvements for wallet-api/zedwallet-beta/WalletBackend this week. A wallet, which has multiple subwallets/subaddresses, is meant to sync virtually as fast as a single wallet, however, with the WalletBackend, this was not the case.

After some investigation, I found out this was because I was using an inefficient data structure to figure out if we had sent an outgoing transaction. After replacing it with a hashmap, we’re back to full speed again when utilizing tons of subwallets. This should make services using wallet-api a lot quicker to sync.

I posted a comprehensive report in #dev_core, if you’re interested.

If anyone else is interesting in profiling some code, the tools I used to profile was valgrind, with the callgrind backend, and kcachegrind for the pretty visualizations. Hit me up on discord if you want exact instructions.” **Zpalm**

[Massively speed up checking key image owner in WalletBackend by zpalmtree · Pull Request #778 ·…Resolves: #724github.com](https://github.com/turtlecoin/turtlecoin/pull/778/files)

![]({{ site.baseurl }}/images/0dajUuCNhNGqJT2_5.png)

The mythical Taintoo

## Rig Of The Week

_Pop in the #mining channel and shoot the breeze with the roughnecks in the mines for the best tips and tricks mining TRTL! If you’d like to showcase your rig, and share your secrets, submit it and we’ll publish one miner per week until we get to everyone._

![]({{ site.baseurl }}/images/0zt5U5_Eb_5Y2ZD8x.jpg)

**heavy-trtl**

**Setup** — Mix bag of 6 GPUs — 2x Polaris cards, 3x Vega cards and 1x Radeon VII. Efficiency is what i seek for. consistent hashrates at lowest power consumption possible == max efficiency. Memory mods, custom clocks, undervolt, i employ them all to achieve my goal.

**Secrets —** cn-trtl is heavily memory bound and you don’t need too high core frequencies like other cn algo variants.

**Secret tips:**  
SET GPU_MAX_WORKGROUP_SIZE=1024 for boosted hashrate.  
set higher worksize 32 for polaris and 64 for vegas to reduce power consumption and also boost hashrate.

**Miner: Teamredminer**  
19.5 KH/s for Vegas at 1285 core, 1100 hbm2 @ 838–850mV  
9 KH/s for Polaris at 1150–1200 core and 2000–2200 Mhz @ 850–900mV.  
38 KH/s Radeon VII at 1560 core, 1200 hbm2 @ 850mV.

**Miner: xmr-stak**  
17 KH/s for Vegas at 1285 core, 1100 hbm2 @ 838–850mV  
8.2 KH/s for Polaris at 1150–1200 core and 2000–2200 Mhz @ 850–900mV.  
30 KH/s Radeon VII at 1560 core, 1200 hbm2 @ 850mV.

Mining rig is inside a grower’s tent with intake and exhaust fans.  
Custom cutouts for ducts from window for intake and exhaust to keep the rig cool during summer. I use a fan controller to regulate noise and fan speed.

**Featured Miner**  
heavyarms1912#4136" I am a sw engineer by profession, hw enthusiast and hobbyist miner

**Hashrate 109 KHs**

## Good First Issues

Once in a while we list an ‘issue’ or bug report on Github as a Good First Issue.. This is for you aspiring devs who might want to snatch some low hanging fruit to get your TRTL Dev role in Discord. No permission is needed, and we’re happy to help, it’s a doer’s market.

![]({{ site.baseurl }}/images/0PyBRcPsnxqy7TTJZ.gif)

we’re cruisin’ through flavor town, baby

## **TRTL Bounties!**

Bounties are easy ways to earn TRTL! If you have some TRTL and need something done, this is where you post it! All bounties need a price in TRTL and a defined goal.

**100TRTL** “I am Offering a Bounty of 100 TRTL if you add a ‘Pay with TRTL’ button to your website (just 2 lines of code) I’ve been working on <https://trtlbutton.com/,> it lets you generate a button and accept TRTL on your website by copying just 2 lines of code! You can check out a demo of a simple html page with 2 lines of code here: <https://trtlbutton.surge.sh/>Feedback is welcome!” **Turtle Max /@mrrovot (github)**

![]({{ site.baseurl }}/images/0h0BDs3Z1fJpu-DX4.gif)

## **Free TRTL Advertising**

- Turtle Pool with Loki Merge Mining from HashVault.pro <https://turtle.hashvault.pro/en>
- TRTLint provides a free API for converting a Turtlecoin address and a payment id to an integrated address. Our HTTP API is easy to use and free for all types of projects, including commercial ones. Made by @fipsi | The Machine <http://trtlint.de.cool/>
- Live in Maryland? Need a 6card open air case? I’ve got one for free. Not shipping cause I just don’t feel like taking it apart. DM Mining4Vets on discord. Need gone asap. Case is one in back with red fans. MINING HARDWARE NOT INCLUDED <https://media.discordapp.net/attachments/548950579632799754/548950923603476481/image0_3.jpg>

![]({{ site.baseurl }}/images/0Q0A4WKz3m9qRO-6P.gif)

**Left**: Snoop Turtle, **Right**: Mayor Wazlo of Exile

## Shoutouts & Thanks

_Special shoutouts to the inmates that stood together in solidarity today by \*not\* taking the amnesty challenge being offered. They’ve decided to take ownership of the inmate lifestyle, and claim #exile as their dojo._

_In their honor, we will hold our shanks at half-rest this Saturday in remembrance of those those who’ve stuck it through unlike the turncoats who never had the stones to stay their sentence and defend their market-talking ways._

![]({{ site.baseurl }}/images/07F-dZBb45V_TDPyP.png)

_You each have two cup-noodles under your pillow, you’ve passed the challenge._

**anon** Please add ‘good first issues’ in some of the JS repos for us noobs that don’t know all the crypto stuff but still want to contribute from time to time

**Turtle Max** Huge shout out to Z and IBMC for their help and feedback to create trtlbutton.com

**Rogerrobers** Shout out to rocksteady for keeping it lit

**Rock** Shouts to the community for crowdfunding Rroger’s taintoo to commemorate his trip to Colombia! Big thanks to the devs completing good first issues. Thanks to the Lethean crew for the hospitality.

**Extra** huge thanks to fexra for putting together the very awesome github.com/fexra/turtle-express-starter for quickly boilerplating turtlecoin powered web applications! you’re the man dude!

**Quasimodo** ‘i love you sierra, don’t leave?’

**Japakar** I’m on phone or I’d post I don’t like anyone leaving haaah

**lifestyles** k12 was a mistake! long live argon2!

**vitalik** To be fair, you have to have a very high IQ to understand Trtl. The protocol is extremely advanced, and without a solid grasp of theoretical computation most of the benefits will go over a typical users’s head.

**greywolf** thanks to Japakar for being an all-around great turtle. he’s always happy and spreading cheer, and is very helpful. plus, he’s always generously spreading tips around the #general chat channel to keep things lively.

**greywolf** thanks to Sierra for giving us some uplifting thoughts to break up the commotion now and then

**anon**fexra is the meme master

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-15-2019/)_._
