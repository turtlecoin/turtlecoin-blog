---
layout: "post"
title: "This Week & Last Week in TurtleCoin (DEC 10th & 17th, 2018)"
description: "We got a little busy last week and a roundup article didn’t get written. Sorry for that, but there’s no time like the present to get this week’s article published! Did you know you can type *news to…"
image: "{{ site.baseurl }}/images/0gDhjU_W75pHMskk5.gif"
date: "2018-12-18T02:07:25.351Z"
---

![]({{ site.baseurl }}/images/0gDhjU_W75pHMskk5.gif)

_We got a little busy last week and a roundup article didn’t get written. Sorry for that, but there’s no time like the present to get this week’s article published!_

**Did you know you can type \*news to get an alert every time we publish these articles? Try it! Go to the chat, and type \*news**

# Developer Updates

![]({{ site.baseurl }}/images/1nIQ6ZtkJkXeg67jwDxgWGg.png)

**TurtleCoin BLOC GUI Miner** — **(dec 10, 2018)** BLOC GUI Miner is a wrapper for XMR-STAK and XMRIG and comes built-in with XMR-STAK. We are working on a new update for our BLOC GUI Miner to support more cryptonote coins and to make it easy for anyone to update a coin or to add-edit a mining pool and much more. The 1st one to be added is TurtleCoin The main interface display the most important informations and links regarding TurtleCoin. We are collecting the data from CoinGecko for each coin and store it into a database where the BLOC GUI Miner has access using a private API. We still have to polish the exchanges stats on the left currently not displaying the right data. But everything else is working. This project is open source so anyone is able to contribute by adding/editing their own mining pools directly using the BLOC GUI Miner GitHub rep as soon as we launch the new version in the next few days. We also have added list of website from the TRTL network, social networks, Coin informations with Price, Network status and more. All the informations are contain in a single file called content.json makes it very easy for everyone to contribute to it. Any feedback is welcome before the official release in few days. Thank you! — **FuriousTeam**

**(dec 17 2018)** — First we would like to say a thank you to everyone for the great feedback we got from the previous release. Some users reported us not to be able to start the BLOC GUI Miner on different systems. We spent the last 3 days improving the miner and today we are happy to announce that the new version is fully compatible with all Windows (7 and 10), macOS (Sierra, High Sierra, Mojave) and Linux (14.04, 16.04, 18.04) operating system. Also there was another problem with macOS users with the last build. We found out that XMR-STAK require Xcode and microhttpd dependencies and this is mandatory. Installing such dependencies can be challenging for some users. For this reason we switched the BLOC GUI Miner macOS version to XMRIG as it is included as a bundle so macOS users will not require to installing anything else beside the actual BLOC GUI Miner. This version should work smoothly. Again we are looking for your feedbacks. This is the most important for us. Feedbacks keep us alive. Thank you. What’s new in 0.0.3 ? BLOC GUI Miner v0.0.3 comes with XMR-STAK 2.7.1 or XMRIG 2.8.3 already built-in, including configuration files for CPU and GPU mining in most of the cases. — Added XMRIG full support for all current and future coins — Fixed content.json file (that cause a major crash on the previous version) — Updated XMR-STAK with latest official binaries v2.7.1 — Replaced XMR-RIG for macOS — 7 binaries available for Windows, macOS, Linux v0.0.3 update details: <https://github.com/furiousteam/BLOC-GUI-Miner/releases/tag/v0.0.3> BLOC GUI Miner Github: <https://github.com/furiousteam/BLOC-GUI-Miner> How to install on windows: <https://wiki.bloc.money/mining/BLOC-GUI-Miner-using/#windows> How to install on macOS: <https://wiki.bloc.money/mining/BLOC-GUI-Miner-using/#mac-os> How to install on Linux: <https://wiki.bloc.money/mining/BLOC-GUI-Miner-using/#linux> How to mine TurtleCoin: <https://wiki.bloc.money/mining/bloc-gui-miner-using/#mining-turtlecoin-trtl> BLOC GUI Miner is a beautiful, easy to use, Graphical User interface for mining multiple cryptocurrencies based on cryptonote. It is aimed at getting people that have never tried mining before with a focus on accessibility, security and simplicity. BLOC GUI Miner support two very popular miner backends: xmr-stak and xmrig BLOC GUI Miner comes with XMR-STAK 2.7.1 and XMRIG 2.8.3 already built-in, including configuration files for CPU and GPU mining in most of the cases. Some antivirus packages detect cryptocurrency miners as malware and will remove the miner as soon as it’s started. In order for the BLOC GUI miner to function, you’ll need to exclude the miner from being scanned by your antivirus software. Download and install BLOC GUI Miner for Windows, Mac and Linux from GitHub Everyone can add their own cryptocurrency to the BLOC GUI Miner as long as it is supported by XMR-STAK and XMRIG. In the same time everyone can add/edit a mining pool into the BLOC GUI Miner. More details here: <https://github.com/furiousteam/BLOC-GUI-Miner/tree/master/coins> Much more is coming soon. **— FuriousTeam**

[furiousteam/BLOC-GUI-MinerAn easy to use Graphical User Interface cryptocurrency miner for crypto night algorithm coins available for Windows…github.com](https://github.com/furiousteam/BLOC-GUI-Miner)

**lite-blocks —** The testnet is going good so far.. we have achieved more than 95% reduction in size of the block being propogated.. some more testing and then you all can benefit from this new feature.. If I am thinking right then following are the benefits/advantages  
1\. less bandwidth usage for those who are running nodes 24/7  
2\. takes less time to reach more nodes compared to current situation  
3\. from the above point we can also deduce that less orphans will be created  
Also iburnmycd is writing an article entirely based on this feature.. I’m eager to see what he comes up with **— Rashedmyt**

[Lite blocks by rashedmyt · Pull Request #623 · turtlecoin/turtlecoinTestnet requiredgithub.com](https://github.com/turtlecoin/turtlecoin/pull/623)

![]({{ site.baseurl }}/images/0hEf8l84rmk2oB6It.gif)

**CN_Turtle Testnet —** Now that PoW algo \[1\] has been announced for block 1,200,000 lets start testing it all out. The project needs some people to run some infrastructure (seed nodes, pool, explorer). We’ll also need some testers to send a few hundred hashes at it and check the miners are all OK as they get updated. In the next day or two we’ll be able to compile the testnet bits \[2\] and even just run straight from containers \[3\] then we’ll aim for an upgrade height for around midnight Saturday UTC specifically block 1,060,600\. So anyone that wants to help out with infrastructure bits please ping me SoreGums#8071 in discord \[4\] to get added to #dev_testnet, everyone has access to view this channel if you’re curious as well. **— soregums**  
\[1\] <https://blog.turtlecoin.lol/archives/proof-of-work-algorithm-change/>  
\[2\][ https://github.com/turtlecoin/testnet/tree/cntrtl-v2](https://github.com/turtlecoin/testnet/tree/cntrtl-v2)  
\[2\] <https://github.com/SoreGums/docker>  
\[3\] [http://chat.turtlecoin.lol](http://chat.turtlecoin.lol/)

[turtlecoin/testnetTurtleCoin Testnet. Contribute to turtlecoin/testnet development by creating an account on GitHub.github.com](https://github.com/turtlecoin/testnet/tree/cntrtl-v2)

![]({{ site.baseurl }}/images/0vfWEPsN3LpjpqWc3.gif)

**TurtleEDU** — The first week of the beta-semester for TurtleEDU is underway! Our test-students have already found a bunch of bugs and corrections, and even a whole section I’d forgotten to upload. Current obstacles are still working out some kinks in the login/email system, thanks to Greywolf for your patience and help troubleshooting in the meantime. Overall, we’ve received positive remarks mostly, and plan to add more revisions to the class before proceeding with the next classes. We’d like to move in a logical order from newbie -> smart TRTL user, and then next we’d like to turn those smart TRTL users into qualified TRTL contributors! If you don’t know what that means, we’re going to be teaching you what you need to know to be able to get the pink role in the chat “contributor”. After that we’ll be moving into development classes so you can learn the way to earn a red “service operator” or bright pink “developer” role! Cowabunga! If you want to know more, go ahead and type \*student in the chat to get your “student” role which gives you access to the EDU_NEWS channel in the chat, your source for all TurtleEDU news and announcements. **— RockSteady**

If you’d like to report an error or correction, please post it in this meta post:[ https://github.com/turtlecoin/meta/issues/133](https://github.com/turtlecoin/meta/issues/133)

If you’d like to check out TurtleEDU, here you go: [http://edu.turtlecoin.lol](http://edu.turtlecoin.lol/)

# Community Advertisements

Turtle (TRTL) Mining Pool by modpool.org Pool Url: <https://turtle.modpool.org/> Pool Fee: 0.8% Features: • PaymentID payments for exchanges, you can directly mine to an exchange that supports this feature • PaymentID, integrated address, subaddress supported • “Slush” payment system ( For details, please check “Payments” Menu) • Stats and hashrate chart per worker • Profit Calculator • E-mail notification when workers down • Pending Balance, Total Paid, Round contribution, Current Payout Estimate • Payment Histoy — Daily • Top 10 miners list • Average 1/6/24-hour Hash Rate • Discord channel : <https://discord.gg/JW3VJfs> • Telegram channel: <https://t.me/modpoolorg>

It’s that time of year again! To celebrate the holiday’s, [turtlenode.online](https://turtlenode.online/) is laying down a special price. Check it out.

New GUI for NibbleClassic! NBXleather linux edition <https://github.com/Sudosups/NBX-GUI/releases>

Join the the ducks in finding turtles. My pool is based on the west coast of the USA. 0.1% fee — [https://trtl.muxdux.com](https://trtl.muxdux.com/)

# TurtleCoin Bounties

**2,000 TRTL** — Image of a Turtle School — Sajo8

**25,000 TRTL** — Integrate TurtleCoin into Keybase client software — if(true)

**1,000 TRTL** — video about how to make pub node. — thcmaster

**250,000 —** Integrate Trezor T as auth/login method into the NEST wallet — Elkim

# Fork Watch!

![]({{ site.baseurl }}/images/0ubPwyoX1l0vn1TTM.png)

**Name of your TRTL fork:**

Aeon Classic

**Github link for your code:**

[Biolith/Aeon-ClassicPrivacy oriented with a mobile focus. Contribute to Biolith/Aeon-Classic development by creating an account on GitHub.github.com](https://github.com/Biolith/Aeon-Classic)

**What is special or new about your network?**

_Privacy Oriented With A Mobile Focus_  
Decentralized digital currency is slowly becoming a normal part of everyday life. Yet everybody’s main internet device continues to be their cellphone, a device with a low-powered CPU and limited available storage. Aeon Classic is about enabling this era, enabling an age where all people everywhere have the freedom to privately send and receive money with whatever gadget they already own.

Aeon Classic team is pleased to announce an android application for shellnet based webwallets. We will be adding additional features in the future.

[Biolith/android-wallet-wrapperContribute to Biolith/android-wallet-wrapper development by creating an account on GitHub.github.com](https://github.com/Biolith/android-wallet-wrapper/releases)

# Shoutouts & Thanks

**Rock** — Rashed, great job on lite-blocks, this will really help the network! I hope your bounty was a fun prize to receive! I’m proud of your work.

**anon —** shoutout to kev and beary for being awesome

**Rock** — Big thanks to Uran and the TurtleCoin China team out there translating our weekly roundup articles to Chinese for our people in the East! As a global project, it is important to us to reach all segments of the community to help our neighbors who speak other languages. I encourage all of you who are part of international communities to follow their example and spread the word to those in your neighborhood. Hello China!! :)

**Rogerrobers —** Shout to chef and capetn keep up the good wrkz work!

**Rock** — Thanks to FuriousTeam for including us in their GUI miner work, this should help out a lot of new Turtles who want to get started mining.

**Morpheus —** Happy Birthday, TurtleCoin! Congrats’ and well done to everyone who played a part in making TurtleCoin the success it is! Radical, Duuudes!

**Rock** — CN Turtle is something I can’t wait to see in action, thanks to IBMCD for your work, and thanks to everyone who helped test it.

**Mufalo —** shoutout to fexra and birfday boi, nice work with edu turtle, lets grow!

**Rock** — Thanks to my partner Fexra for helping out with TurtleEDU! and thanks to the students who are in our first beta semester finding bugs for the EDU team! Thanks Greywolf for helping troubleshoot our login and email system.

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-last-week-in-turtlecoin-dec-10th-17th-2018/)_._
