---
layout: "post"
title: "This Week in TurtleCoin (Nov 12, 2018)"
description: "This week was one of the best yet! Between playing the games you guys made with your TurtleCities pages, and ones you wanted to watch on TwitchTurtle, I’m spent! Awesome community participation this…"
image: "{{ site.baseurl }}/images/0f0oRpQ8QBWBOULwf.png"
date: "2018-11-13T05:01:34.352Z"
---

![]({{ site.baseurl }}/images/0f0oRpQ8QBWBOULwf.png)

This week was one of the best yet! Between playing the games you guys made with your TurtleCities pages, and ones you wanted to watch on TwitchTurtle, I’m spent! Awesome community participation this week, and we’re really looking forward to next week!

# Developer Community

![]({{ site.baseurl }}/images/0z7TQqabnlWJH4k2h.png)

**Trtl Driver** — As turtles we all have a need for speed, scratch that itch by playing the “Turtlefied” version of Yu Suzuki’s arcade classic “OUTRUN”. Discover this and many more games @ “games.turtacus.com” — a showcase for all the diverse talents of the TRTL community. If you want your game/ project featured or are interested in learning more about game development, please message me @ Trt.Simulator@gmail.com or drop into the TRTL Discord! **— Oiboo**

![]({{ site.baseurl }}/images/0inMxKz0u0NXPJBB2.png)

**TurtleCities** — Wow, it has been a big week for all of you that put up homepages on TurtleCities! For those of you that don’t know, we made a just for fun project last week that lets people sign up for a single floppy disk worth of web hosting for an old school home page and to show the internet just how cool you can be with only 1.44mb to express yourself. I’m still deciding on “upgrades” to offer, but currently thinking about doing a “Dual density floppy upgrade” for 2,000 TRTL, and I’d like to see what adding some shell accounts to certain users would be like. The obvious next step is to release the BBS system I’ve been tinkering with…. But that’s another story :D **\-RockSteady**

![]({{ site.baseurl }}/images/07V_Kk0SmaRGBnYDr.png)

**TurtleEDU** — I’ve completed all of the course material for the first course on TurtleEDU, which I’m going to call “TurtleCoin 101”. It’s a class that will take someone who is new to cryptocurrencies and turn them into a certified TurtleCoin user by the time they finish. It doesnt take long, and the class is divided up into easy sections. I’d like to add some finishing touches, but I get the feeling I may be overdoin it, so video/audio content might wait until after the beta launch for people with the “student” role. Remember, if you’re interested in being a trial user of TurtleEDU, be sure to type `*student` in the discord to automatically enroll you in Turtle School :D  
The next classes I'd like to work on are "Contributor 101" which will guide the user through how to use Github for version control to create and modify guides and wikis, and then "Developer 101" which will be a guided tutorial to using the TurtleCoin API using the docs on [https://api-docs.turtlecoin.lol](https://api-docs.turtlecoin.lol/)  
Fexra is still working on the visual theme for TurtleEDU, and we'd like to get it skinned up before you guys get to try it out on December 9th, our one year and 1 million blocks anniversary! **\- RockSteady**

![]({{ site.baseurl }}/images/0lBfB94ktWYD2sk9Q.jpg)

**Core Team Update** — A new core developer has been officially added to the team. He has significant amounts of contributions to the core suite and is the project leader behind the Golang port of the TurtleCoin Core Suite — We are very pleased to introduce Rashed to you guys :) You are probably already well acquainted with seeing his name in the roundups and hearing about him in podcasts, and we’re very excited to bring him aboard. Great job, sir! **— RockSteady**

[Trtl Arcade | WelcomeOnline games for the TRTL communitygames.turtacus.com](http://games.turtacus.com/)

![]({{ site.baseurl }}/images/0OrJLpwLVaNrZ3mMl.png)

**lite-blocks** — This is the TRTL version of XMR’s Fluffy Blocks which is being implemented to increase the propagation of blocks in the network in a much efficient and faster way. Work is progressing slowly day by day as I am in middle of my semester exams.  
So what are lite-blocks? We all know that new transactions propagate throughout the network and are stored in the transaction pool of every daemon.. whenever a miner finds a block the daemon removes those transactions from the pool and adds them to the block and then propagate that block throughout the network.. you see transactions are a heavy thing.. they make up most of the size of the block.. it is just an overhead to send the transactions again which the other daemon already has.. also since it increases the payload size it would take time to propagate it throughout the network.. To solve this problem instead of sending the block with all those transactions we just send their hashes which are much less in size.. the receiver checks for those transactions in its transaction pool.. if it has all of them it creates the block by itself and adds it to its database.. but if it couldn’t find any of those transactions.. it requests the sender to those missing transactions only.. hence the lite-blocks essentially contain the block header and the transaction hashes which are present in it or it contains the block header along with the transaction hashes and the requested transactions.. this technique will help reduce the payload for the propagation of block throughout the network and hence result in much healthy network and I guess less orphans too **— rashedmyt**

[rashedmyt/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - rashedmyt/turtlecoingithub.com](https://github.com/rashedmyt/turtlecoin/tree/lite-blocks)

![Image result for travis ci](https://miro.medium.com/max/60/0*dtoRAyGVu6HtFSdF.png?q=20)

![Image result for travis ci](https://miro.medium.com/max/1284/0*dtoRAyGVu6HtFSdF.png)

**Windows on Travis** — Got bored by studying for my exams and thought lets take a look whether travis has given support for c++ projects on windows or not. To my surprise, they have supported it very soon and I thought lets get the work started. After working for a couple of hours to figure out how to get started and get things done, also not to forget the long waiting times for the build to just see the red error messages. I have finally managed to get the build working perfectly and deploying. Thanks to iburnmycd and zpalmtree for helping me with disabling the builds to just test the windows build. **— rashedmyt**

[rashedmyt/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - rashedmyt/turtlecoingithub.com](https://github.com/rashedmyt/turtlecoin/tree/windows-travis)

![]({{ site.baseurl }}/images/0Ghy8Cmv1cGykkVBs.png)

**trtl.rocks** — Here is a quick breakdown of what I’ve done on [http://trtl.rocks](http://trtl.rocks/) over the last two weeks **— andrew | trtl.rocks**

• Restructured the database  
• Added fuzzy search and pagination to the nodes and pools page  
• Added node fees to the node table  
• All The Pools — expanded the pool service to grab data from forknote and node.js pools, as well as cryptonote.social  
• Added pool fee types, when available  
• Updated the pool hashrate graph to display unknown hashrates  
• Fixed mobile nav

[TurtleCoin ExplorerExplore historical and live block, node, pool, and transaction data for TurtleCointrtl.rocks](http://trtl.rocks/)

![]({{ site.baseurl }}/images/0hmzieji91qI8qYb6.jpg)

**TurtlePay™ —** Quite a bit of progress has been made this week in the Blockchain Data Collection Agent (BDCA) with the sole purpose of collecting and caching the blockchain in a database friendly way. Building a strong backend distribution system for TurtlePay™ is paramount as the scale and flexibility is at stake. Returning data as quickly as possible gives us the ability to scale to massive unprecedented levels seldom seen in Blockchain applications. Initial testing has shown the ability to provide data to the wallets at a rate of about 100,000 blocks per minute. The payloads provided to wallets are substantially reduced in size to include just the needed information for scanning for funds sent to our wallet(s). As a byproduct of the streamlined payloads it is possible to create a fast, efficient, and versatile block explorer built on this database backend. Look forward to more information to come in the coming days and weeks and keep up with the latest information in #dev_turtlepay **— IBurnMyCd**

[TurtlePay/blockchain-data-collection-agentTurtlePay™ Blockchain Data Collection Agent (BDCA) - TurtlePay/blockchain-data-collection-agentgithub.com](https://github.com/TurtlePay/blockchain-data-collection-agent)

![]({{ site.baseurl }}/images/0aTqY0bKQfqR2mZhj.png)

**Swanson Clicker** — Swanson Clicker has come a long way in a short amount of time! Thank you to all the \~76 unique users who have clicked Swanson whether that would be 1 time or 1,000 times! Hopefully your Pineapple Farms and Snail Racers are doing great. In the future, I will be attempting to gracefully implement items and more statistics so bear with me if you lose your progress. If you have not tried Swanson Clicker yet, then you’re missing out! Special thanks to Oiboo in discord for this awesome title-card for Swanson Clicker. **— Xaz**

[Swanson ClickerEdit descriptionswansonclicker.com](http://swansonclicker.com/)

![]({{ site.baseurl }}/images/09Eq1c-\_xOEb7NSKi.jpg)

**WalletBackend / WalletGreen rewrite —** Finished rewriting zedwallet this week with the new wallet-backend I’ve been working on everything seems to work well. Apparently it has some issues on Windows. Shouldn’t be too much effort to fix, though. I started writing some documentation on the wallet file encryption format, and the wallet JSON format. You can get that here — <https://github.com/turtlecoin/wallet-file-interaction> if you’re interested in interacting with wallet files manually, perhaps to build your own wallet backend implementation. I’ve got some examples of how to open a wallet file up there, currently in C# and C++. If you’ve got a favorite language and you think you’re likely to want to be able to open wallets without the help of an RPC interface, let me know, and I can probably code up an example for that language too. Next I need to get turtle-service rewritten, so you can make API calls to it from all your favorite languages. Oh — I finished writing that article I was talking about on how transactions work. Just giving it a bit of a review then it should be ready to publish. Thanks to IBMCD for reviewing my code :)) **— Zpalm**

![Thanks for reading.](https://miro.medium.com/max/60/0*pkskRAh4y8gP69JB?q=20)

![Thanks for reading.](https://miro.medium.com/max/1344/0*pkskRAh4y8gP69JB)

**Article** — I wrote that article on transactions I was talking about in past roundups — you can check it out [here](https://blog.turtlecoin.lol/archives/how-a-transaction-is-born-and-how-wallet-syncing-works/). It goes into depth on how wallet syncing works, and how a transaction is made — it’s a bit complicated, but hopefully a few people can learn something **— Zpalm**

[How a transaction is born, and how wallet syncing worksLets say Bob decides to do some solo mining, and gets lucky one day. Maybe he mined block 900,000\. Bob got 29,013.99…blog.turtlecoin.lol](https://blog.turtlecoin.lol/archives/how-a-transaction-is-born-and-how-wallet-syncing-works/)

# Community Bounties

**2,500,000 TRTL —** Submit a PR, and have it accepted, to add MULTI-SIG wallets to TurtleCoin and receive the following bounty. **— TurtleCoin Core Development Team**  
+500k from IBMCD  
+500k from Zpalm  
+500k from RockSteady  
+500k from fexra  
+500k from Slash-atello

**1,500,000 TRTL —** Submit a PR, and have it accepted, to add RINGCT to TurtleCoin and receive the following bounty. **— TurtleCoin Core Development**  
\+ 500k from IBMCD  
\+ 500k from Zpalm  
\+ 500k from fexra

**75,000 TRTL** — I need a quick site done up with a simple (very simple) shopping cart interface that does the following **— GNU/Ashmedai**

1. guest selects “purchase access”
2. guest is given an address and payment ID to send the amount of TRTL to
3. once TRTL is received, guest is granted the ability to download a file up to 5 times.
4. upon limit reached, access to file is denied.  
   **Bonus bounty: +25K TRTL if TRTL.Services is used.** Project will be used to host a TRTL blockchain bootstrap.

# Community Advertisements

0 fee nodes; greywolf London turtlenode.me:11898; and greywolf Germany turtlenode.co:11898

Looking for a rock solid, highly available public node to use with your wallet? Look no further than the ORIGINAL TurtleNode.io. No, our fees are not the cheapest in town but we’re the oldest, longest running, public TurtleCoin nodes in existence today. Why fight with the rest when you can enjoy the best! — <https://turtlenode.io/>

Interested in mining on a set of pools, with 3 locations worldwide? Look no further than [http://turtlepool.space!](http://turtlepool.space/!) Turtlepool is the oldest turtle mining pool, only a week younger than TRTL itself! Locations are: Hong Kong (with direct china route), London, and Dallas. Support offered in English and Russian — [http://turtlepool.space](http://turtlepool.space/)

Mine2Gether invites you to our weekly Blockchain Bingo  
The next Blockchain Bingo is Saturday Nov 17th @ 18:00 GMT in our discord #bingo channel. Community super fun, open to everyone, and completely free to play! It is a variation and similar to traditional bingo, and uses the turtle blockchain to draw the numbers. Everyone is welcome! 25K TRTL prizes, 100K jackpot, slots mini game, and more!  
Each winner will also direct the amount matching their prize towards the turtle development bounty of their choice. (for example, if you win 25K we will direct an additional 25k to the bounty of your choice on your behalf.)  
Hope to see you there!  
**Bingo Site:** <https://bingo.mine2gether.com/>  
**Bingo Discord:** <https://discord.gg/AT3AAxV> **(#bingo channel)**  
**Converted date and time:** <https://www.timeanddate.com/worldclock/fixedtime.html?msg=Mine2Gether+Blockchain+Bingo&iso=20181117T18>

# Shoutouts & Thanks

Oiboo — Big thanks to Rynem for the Webspace! :D ❤

GNU/Ashmedai — Shout out to ison for his wonderful work on the WalletBackend re-write. It’s times like this that I get excited for what the future holds for the project!

IBurnMyCD — Yo to the AmityCoin crew for their first week running the first consistently running Soft Shell mainnet.

rashedmyt — Thanks to RockSteady and the entire community for recognizing me as one of the core developers..

mufalo — Special thanks to zeto sama for being so nice when i have dumb logic-code troubles

Xaz — Special thanks to Oiboo for linking to Swanson Clicker on his arcade site! 🐢🐢🐢

arms — Shoutout to all the devs and community members for constantly building great things and being awesome!

anon — thanks for keeping the chat an education place for users and trader-free.

# Fork Watch!

![]({{ site.baseurl }}/images/0yauFzRxTVvJLLiiM.png)

**Name of your TRTL fork:** CyprusCoin

**Github link for your code:** <https://github.com/CyprusCoinClub/CyprusCoin>

**What is special or new about your network?:**

CyprusCoin completely focused on Offshore business and investment market. We have built CyprusCoin as a fast emission Cryptonote coin that aims to provide users a secure environment to handle their funds. On the technology side we are trying to have an advanced but at same time easy to use interface that will help everyday users to manage their funds safe and securely.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-nov-12-2018/)_._
