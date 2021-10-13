---
layout: "post"
title: "Out of the Shell #5: Iburnmycd"
description: "Welcome to the fifth installment of Out of the Shell, a series of interviews with the developers, designers, and doers behind TurtleCoin…"
image: "{{ site.baseurl }}/images/018SFPm6T3q00QC49.png"
date: "2018-04-12T02:37:05.064Z"
---

![](https://miro.medium.com/max/2400/0*18SFPm6T3q00QC49.png)Giordano’s Chicago Style Deep Dish Pizza

_Welcome to the fifth installment of Out of the Shell, a series of interviews with the developers, designers, and doers behind TurtleCoin. This is @gigantomachia and I’ll be your host._

After a bit of a hiatus, I’ve returned to drop a new interview with another outstanding member of the TurtleCoin community: [@iburnmycd](http://twitter.com/iburnmycd) . Anyone who’s recently hung out in the TurtleCoin discord server will recognize [@iburnmycd](http://twitter.com/iburnmycd)’s handle. Despite working 80+ hours a week as a chief technical officer at a national managed service provider, he still seems to active on discord 24/7.

His real name is Brandon and he lives in “a small town” somewhere in Ohio. Over the last few months, Brandon has taken a deep dive into TurtleCoin and has become a major contributor to the community. He created <https://turtlenode.io/> as a free set of public nodes after identifying a need and is currently working on developing a set of native TurtleCoin libraries in a number of programming languages to enable more developers to build apps on top of the network.

Brandon and I discuss what drew him to the project, what he’s working on, where he sees TRTL heading, and how what started as finding a cool coin to mine has become an all-consuming hobby.

> **Tips welcome:** TRTLuxvBFVNSxovAp3c9C8h8dUttA4sP8hHELDQJXsQZ7JcKfnn3sLkUPGQgQBkvvhXFfAErUqmf52BzyqFaHhEHicRNLnXYfRj **(Gigantomachia)**

**How’d you first learn about TurtleCoin?**  
I actually found it through [cryptunit.com](http://cryptunit.com/) as I’ve been operating a smallish pool of miners using some old hardware and would check the going rates every few days. TurtleCoin popped up one day and my wife and I laughed a bit at the name. After checking it out we were intrigued given the how early in the project it is and we haven’t looked back.

**Your wife is involved in TurtleCoin, too?**  
She’s involved, yes. She’s working on some cool artwork for @**fexra’s** web wallet.

**What’s her handle?**  
@**shelly**

**When was it that you guys got involved?**  
It looks like I started mining TRTL on Feb 8th, 2018\. I recall I watched the hashrate surge and drop for a few days before that. I’d have to guess I found it around Feb 5th, 2018.

**What was it about TurtleCoin that initially drew you in? What did you find intriguing about it?**  
I remember when I first heard of Bitcoin. I mined a little way back when as a gaff, ended up dismissing it like many others, lost the keys, and cried in late 2018\. Once I found TRTL, I felt like there might be a chance to redeem myself. Honestly, once I joined the Discord, I was hooked. There is an awesome community built around a blockchain in its infancy and I saw ways that I can help. I was also in dire need of a hobby as my professional life tends to consume me.

![]({{ site.baseurl }}/images/0BKAB3em6HG6rvxfF.PNG)

**What does that professional life entail? What’s your day job?**  
I’m the Chief Technical Officer for a national managed service provider that provides WAN, Voice, VoiP, TV, WiFi, Project Management, and Photo Support services. I lead teams of developers, network engineers, network support staff, field technicians, project management teams, R&D teams, and everything in between.

**How did you approach getting more involved in the community beyond mining? What was the first project you dove into?**  
I’m constantly hopping between my desktop at home, my desktop at work, and my laptop. Keeping three different nodes synced seemed like a pain and I don’t carry around flash drives. So I setup a remote node in one of my personal server farms to use and that worked out well. I knew that there was a remote node available at **daemon.turtle.link**; however, I had intermittent success in syncing my wallets against that. Seeing a gap, I figured I could help fill it. That’s why I created <https://turtlenode.io/> as a free public set of nodes. In conjunction with that, the TurtleCoind binary would hang up, freeze, or crash at times and that wasn’t up to par with the type of services that I habitually run. As a result, I’ve been working on the turtlecoind-ha project that I created to help keep the nodes sane, in a running state, and current on the blockchain. I’ve got some big ideas that I share with the rest of the community and chime in where I think I can add value. The community as a whole keeps me enticed and wanting to help however I can.

**Tell me more more about the turtlecoind-ha project. What’s it about?**  
In short, turtlecoind-ha is a service wrapper that actively monitors and interacts with the TurtleCoind program to make sure that it’s actually responding (not crashed) and is synchronized with the network. For anyone that likes to start the TurtleCoind program and leave it running, it can help tremendously in making sure that you’re always synchronized with the network. No waiting for TurtleCoind to sync when you just wanted to check your wallet balance quick.

![]({{ site.baseurl }}/images/18_3mJdmqZK9rKOloflTJ6A.png)

Tired of syncing? Try TurtleNode! It’s awesome! It just **works.**

**What’s your favorite pizza?**  
That’s a toss up between Chicago-style Deep Dish Pizza (_Giordano’s_ or _Gino’s_) or the coal-fired variety (_Anthony’s Coal Fired Pizza_). Either way I lean towards heavy on the meats and light on the veggies. Whenever someone I know makes a trip to Chicago, I bribe them for a deep dish.

**When you’re not working or hanging out in the TurtleCoin discord, what do you like to do for fun?**  
My wife and I try to relax. Whether it’s hanging out with our dogs, watching movies, or trying to find an event to attend we try to use our downtime wisely. That’s not as often as it probably should be because I typically work 80+ hours a week.

> **Note from RockSteady:** That 80hrs+ figure seems a bit low.\[Citation Needed\]

**What’s next for you and TurtleCoin? We talked about the public nodes you’ve set up and the turtlecoind-ha project, but what are some other big picture ideas you have for the coin and your involvement in the community?**

What’s next: I have some work to do on the turtlecoind-ha package to add some more sanity checks as well as an out of band management interface for remotely controlling the node to allow for a centralized master control server. This code will help to maintain the [**TurtleNode.io**](https://turtlenode.io/) public nodes as the service continues to grow. I would then like to apply some of the same concepts to walletd.

Big picture: Ultimately, I hope to find the time to work with a few others to abstract the cryptonote and cryptonight functions to a point that it becomes easier to build tools that interact directly with the network instead of having to rely on external programs (i.e., TurtleCoind, simplewallet, walletd). Enabling more developers to work directly with a set of native TurtleCoin libraries in languages like C++, Node, .NET, etc. would provide a massive catalyst for the development of additional TurtleCoin applications and solutions. I’ve also discussed the ability to abstract the blockchain storage to other backend database systems that would help enable Service Providers to run high-end services with TurtleCoin. I’m excited as the prospect of what the community can put together when we all work together.

**That’s a good lead-in to my next question, which is where do you see TurtleCoin going in the future? In 5 years, are we still just going to be using it to tip peple on discord? Or do you see real-world use cases coming down the pike?**  
Visualizing the mass adoption of any cryptocurrency is difficult. While I believe that the technology has considerable value to the global economy, whether the cryptocurrency community wants to admit it or not, I believe that for mass adoption to occur strong partnerships with government and banks is required in the long term. Accessibility is one of the most important aspects of any currency. While the decentralized nature of cryptocurrency is one of the major drives behind it; there is something to be said for the fact that FIAT is very easy to work with (aside from regulations).

With continued strong community and development support behind TurtleCoin, I believe that the project can help shape the discussion on how cryptocurrency cracks the mass-adoption barrier. Driving for the ability to extend the use of TurtleCoin to other areas in a way that lowers entry barriers, provides a means to strong integrations with third-party systems, and makes it as easy as FIAT to use is my hope for the project in the long term. The TipBot is just the tip of the iceberg in that regard. With the project still being in it’s infancy there are many paths that the project can take. Each community member has their own take on what’s possible for the project in the future and under the core team’s guidance, I have faith that TurtleCoin will prosper.

I can’t speak of any use cases coming down the road any time soon; however, I’ve had some conversations recently with some of the community developers that lead me to believe that there is strong support for working towards the ability to create a TurtleCoin Automated Clearing House (ACH) type system that would allow for the building of a Payment Gateway. Development of these items would help merchants to adopt TurtleCoin as an accepted payment method. The WooCommerce plugin provides a step in this direction and I’m excited to see it used in online stores.

**You mentioned you were operating a small pool of miners when you discovered TurtleCoin. How long have you been into crypto?**

If I recall correctly, I originally took a look at BTC back in mid-2011; however, as I mentioned before, I saw it as a novelty and something to fiddle with. I saw it as one of those pet projects that teams create and then let die eventually. I largely ignored it for a number of years as I focused on my career and other personal development. Some of the news that was kicking up in early 2017 piqued my interested and I started reading a little bit here and there on the developments. I kept the entire crypto concept at arms length last year until late October when I started to look at things a bit more closely. By the time the bubble jumped, I knew it was too late to get in for that round of gains — and mining it without serious investment was laughable. I saw movement in the Altcoins markets and have a whole bunch of spare hardware laying around that I figured could be put to good use. Most of it has been left powered on in racks or under my desk and I figured I might as well make some money with it. From there, most of my involvement is, at its core, my way of helping crypto succeed to help drive eventual value and adoption.

**You mentioned some of the projects or initiatives you’re working on or have in your sights. Any areas where you’re seeking community input? Any opportunities for people to get involved if they want?**

Excellent question! I’d love to garner some input from those in the community regarding technical writing, documentation techniques, and other such functions. These things are paramount to the successful development of any project. In addition, those familiar with any programming languages would be more than welcome. The entire community benefits from the combined experience and knowledge of anyone that brings concepts, discussions, or development talent (in any form) to the group. At the risk of sounding like a hyped up CEO on a stage at a developer’s conference, the more “DEVELOPERS! DEVELOPERS! DEVELOPERS!” we have working towards any of the community’s goals we have, the better off we all will be as a group.

**Anything you’d like to add?**

If people are interested in helping out, they should check out the **#bounties** channel on discord. There are some rather high value bounties currently open that are up for grabs for anyone that wants to put a bit of effort in. If you don’t see anything you think you can help with, certainly ask if anyone has anything they would like help with. You may not get a bounty for it, but putting the effort forward to show that you want to help will get you started in the world of TurtleCoin development. We look forward to many new turtles.

> **Tips welcome:** > **TRTLv1pacKFJk9QgSmzk2LJWn14JGmTKzReFLz1RgY3K9Ryn7783RDT2TretzfYdck5GMCGzXTuwKfePWQYViNs4avKpnUbrwfQ (Iburnmycd)**

**Note from RockSteady: Great interview, Iburnmycd! You’ve been here just a short time and have contributed some big changes, I hope to have you around much longer :) Good job with everything. We’re all clapping for you!**
