---
layout: "post"
title: "Getting TRTL Network Ready For Enterprise w/ Fexra from TRTL Services"
description: "fexra thanks for agreeing to the interview. I think this one will really put some perspective out there for people who are skeptical about the enterprise capability of the TRTL Network. If you had to…"
image: "{{ site.baseurl }}/images/0qmJdcX_61SptwUnC.jpg"
date: "2018-09-28T18:26:03.951Z"
---

![YOU GET AN API](https://miro.medium.com/max/1240/0*qmJdcX_61SptwUnC.jpg)

# **RockSteady (TRTL)**_:_

fexra thanks for agreeing to the interview. I think this one will really put some perspective out there for people who are skeptical about the enterprise capability of the TRTL Network. If you had to shill me your hosted services in 30 seconds or less, what would you say?

**fexra | trtl.services**_:_

Hey rock. Thanks for taking the time to do this interview with me. TRTL Services provides a simple interface and RESTFUL API for developers to start building with TurtleCoin right away. It takes care of all the under the hood infrastructure such as hosting and maintaining the turtlecoind and turtle-service so developers can focus on what matters; building decentralization applications on the turtle chain!

**RockSteady (TRTL)**_:_

That’s really cool, to help us visualize this, can you give me a few examples of what a user would use the system for?

**fexra | trtl.services**_:_

Right on. The possibilities are more or endless; ranging from integrating TurtleCoin you mobile apps and games to creating your own bookmarking tool :). To get more specific: some of your readers may remember the web wallet that I’ve been working on. The code that TRTL Services runs on is more or less the backbone of that web wallet, but separated and hosted as a service. The web wallet (turtlewallet.lol) is fully powered by TRTL Services and a good example of what could be build with it. Currently, I’ve got a few developers and merchants waiting for the release. One wants to build a TRTL Messenger app; another wants to start accepting TRTL on their online store without worrying about the technicals and a third wants to integrate TurtleCoin as a currency in a mobile game he’s building.

![APIS everywhere](https://miro.medium.com/max/60/0*Ykq6bCDY4ElUc68j?q=20)

![APIS everywhere](https://miro.medium.com/max/1000/0*Ykq6bCDY4ElUc68j)

**RockSteady (TRTL)**_:_

So it’s not necessarily a service where you could point and click deploy something like a pool or explorer, right?

**fexra | trtl.services**_:_

No, currently we only offer Turtle-Services access via API, but what you’re hinting at is ultimately the goal and is something I’m working on with Slash-atello. The idea is for users to be able to deploy their own turtlecoind/turtle-service daemons in Dockerized containers in minutes which they could connect their pool or explorer too.

**RockSteady (TRTL)**_:_

That’s pretty cool. How do you charge for something like that? I’m guessing people get allotted a certain amount of API access- I could be wrong. Is there any plan for how something like this can be priced and paid for yet?

**fexra | trtl.services**_:_

Currently, Turtle-Services charges a 2.1% convenience charge on every transaction completed with the API with no other limits — it’s really up to the developer to decide who carries that cost. As the project expands and the userbase grows I will be looking into diversifying prices. I have some ideas that would incorporate the flat node fee and am also looking at offering packages, but for now I think it would be wise to keep it simple and not create walls that may get in the way for developers.

**RockSteady (TRTL)**_:_

How are you able to charge a percentage convenience fee on each transaction? I imagine that’s quite difficult.

**fexra | trtl.services**_:_

When the user creates a new transaction with the API, the API splits that up in two transactions. One for the intended receiver who and one for the fee wallet. Hence when sending a transaction with the API, you will have to calculate in the service fee beforehand. There will will be for the API in Node.JS, PHP and Python that come with tools to handle this.

**RockSteady (TRTL)**_:_

That’s quite the undertaking. How long until people will be able to get their hands on this service? We know the web wallet, which as of this writing, still isn’t released, is there a time frame when the API services that rely on the completed backend of it will be ready?

![Image result for freedom is a meme, only the intelligent survive](https://miro.medium.com/max/1000/1*i9_8BgHrQREedxmcO4sHTw.png)

**fexra | trtl.services**_:_

Yes it is indeed. Code wise everything is there ready to go online. I’m currently, with the help of Slash-atello, setting up the backbone; mainly spinning up servers and putting the daemons behind node balancers. The web wallet will go live first and will act as a kind of test for the Turtle-Services network. While this is happening, a few developers will get access to the Turtle-Services API to start building and testing their apps; they can expect to start building this weekend :). Depending on the amount of problems that will occur, I expect some, Turtle Services can go public soon afterwards.

**RockSteady (TRTL)**_:_

That’s really cool. If someone reads this interview and says “wow man, I want to get involved in this”, where can I point them? Is there a repository where this is being worked on currently so people can pitch in? If someone is a developer of their own apps, is there already a learning resource or website or something where they can grab an example piece of code and start working?

**fexra | trtl.services**_:_

Yes! The API documentation is already available <https://trtl.services/documentation> — however the repository is still private. I been promised a security audit by IBurnMyCD, which I would like to wait for. However, the Node.JS, PHP and Python wrappers will be available at the time when the first developers get a go at it. The repo for the web wallet will go public too, and will act as the first demo app utilizing the service.

![Image result for im running out of memes here](https://miro.medium.com/max/60/0*QkmoXhsN3hiK-DoW.jpg?q=20)

![Image result for im running out of memes here](https://miro.medium.com/max/950/0*QkmoXhsN3hiK-DoW.jpg)

**RockSteady (TRTL)**_:_

This is all coming together very nicely, good job to you and IBMCD, I know I’ve been watching you guys work on this for quite some time. What made you finally break off this bit of functionality from the main web wallet? Surely you saw a need for it, but what was the moment when it clicked that you needed to build hosted services? What types of applications do you see people deploying initially, and what do you hope they use it for down the line when it gets more popular?

**fexra | trtl.services**_:_

Thanks man, it means a lot

Well since late January my ultimate vision of the web wallet was to be a bit more than just a simple online TRTL wallet. I got the idea of building the web wallet because of my first project, [Woo-Turtle](http://github.com/turtlecoin/woo-turtle), which allows WooCommerce powered e-commerce websites to accept TRTL. I realized quickly that although this was a neat plugin, most people that run an online store are well … not so tech savvy — and so I came up with the idea to build an online wallet that comes with API integration and third party integration plugins to allow merchants to accept TRTL in ease. As I started working away web wallet got quite bloated and it became difficult to have an oversight on the code and IBMC suggested to turn it into two standalone projects, one powering the other, which honestly is the best advice I have still received from him so far

I expect most of the customers to be online merchants and mobile app developers that are looking for a quick and easy way to integrate TRTL as payment option on their store, game or app. I’m the most excited about integrating TurtleCoin in mobile apps and games and see an huge market potential for that. As it gets more popular I would love to see apps completely build around the TRTL Network but that will also depend on the development of Karai and if Turtle-Services can keep up with the demand.

**RockSteady (TRTL)**_:_

Ah that’s making a lot of sense now, with your vision for the future. Will this be powering the first TurtleCoin <-> Karai <-> Athena exchange also? Until we get smart contracts going on Karai and cross-chain transfers on Athena, we will likely need that as a means of exchange between the three. I’m very optimistic about your API services and look forward to see what gets built with it. Who are the app developers who have helped you so far with the core system, and who are the developers who will be the first ones to develop apps, as testers on the platform? We should recognize their work here, because I’m sure it’s quite the responsibility.

**fexra | trtl.services**_:_

I like your thinking! Although that is certainty possible with Turtle-Services, I think IBMC’s TurtlePay™ project may be better suited for that — I’m sure if we put our heads together we can come up with something :) Thanks Rock, it means a lot! All the code has been written by myself so far and I must say it has been quite a journey the last half a year… but I have learned so much! None of this would ever been possible without the countless hours of advice, help, guidance and patients from @Ereptor, @Bebop (TRTL), @rockSteady, @IBMC and @SoreGums, and the hundreds of others who have helped me beta test and have provided feedback, bugs and exploits. Currently three devs: @fruktstav, @sajo and @AndΞrson one merchants: @HamHands and a pool owner @Cision — turtle.atpool.party will get early access. I would also like to give a shoutout to HamHands who has been so generous to cover the costs for my servers for a month when I was in trouble

![:t_heart:](https://miro.medium.com/max/60/0*JJ16CuATN4jegG3G?q=20)

![:t_heart:](https://miro.medium.com/max/128/0*JJ16CuATN4jegG3G)

Honestly TurtleCoin is one of the, if not, greatest online communities I ever been part of.(edited)

**RockSteady (TRTL)**_:_

Sounds great, I look forward to seeing the developer guides that are coming out soon, and I can’t wait to write about the first services that get deployed on your system. Good luck! Is there anything else you want to mention?

**fexra | trtl.services**_:_

Thanks! I think we pretty much covered it for now. All I can say for now is keep your eyes peeled for the developer guides!

**RockSteady (TRTL)**_:_

great!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/getting-trtl-network-ready-for-enterprise-w-fexra-from-trtl-services/)_._
