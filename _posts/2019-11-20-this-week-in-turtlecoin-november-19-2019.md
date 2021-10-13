---
layout: "post"
title: "This Week in TurtleCoin (November 19, 2019)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0hwrXJFZ4qvR-nlH-"
date: "2019-11-20T05:19:57.699Z"
---

![]({{ site.baseurl }}/images/0Kg_hIx2W3XuBx1RT.gif)

![]({{ site.baseurl }}/images/0hwrXJFZ4qvR-nlH-)

Teacup made this

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

![]({{ site.baseurl }}/images/0EhwgR4-nm2NqE8Gd.png)

## **First Annual TurtleCoin Crypto-Hackathon!**

![]({{ site.baseurl }}/images/0prVRYtqKlJU7u9tl.gif)

Big shout out to all the teams who’ve registered so far for the hackathon! We still have about 10 days for new team signups so whether you’re on your own or have a crew of friends, you still have time to sign up!

Also, when you sign up, don’t forget to let us know if you want to be interviewed and how to get in touch with you!

## [Click here to signup your team!](https://docs.google.com/forms/d/e/1FAIpQLSe8whOEaS_CR_WbrzJwJ-LzRKyI4YXIRnl3jd34HHa5Tk_hJA/viewform)

[TurtleCoin Crypto-Hackathon 2019To celebrate our 2nd year as a community on December 9th 2019, we are sponsoring the first annual TurtleCoin™…crypto-hackathon.com](https://crypto-hackathon.com/)

**CantiLib / CS-TurtleCoin**

Another overdue update. I set aside a day to write up everything that goes on while talking to and syncing with an existing node, getting back to my reverse-engineering roots. Since then, I’ve been working on implementing these communications into CantiLib. This mean that soon™ a CS-TurtleCoin node will be able to act as a functional peer on the network, able to relay and propogate data to and from other nodes. I have also moved to utilize EF Core 3.0 for local data storage, and have rewritten block caching to suit, which means that a user will be able to choose which database type they’d like to use to store their synced data. At the moment, I have implementations for SQLite, MSSQL, Azure Cosmos, among others. Once these changes are completed and pushed, there will still be a _lot_ left to add to get it to the same level as an existing C++ node, such as fleshing out API functions, but it’ll be a big step forward in my daemon rewrite.

**Canti**

[turtlecoin/cs-turtlecoinThe wind howled by me As I sat and watched the world; All but powerless You need the dotnet command line tools. This…www.github.com](https://www.github.com/turtlecoin/cs-turtlecoin)

![]({{ site.baseurl }}/images/026I5CtPau3vlB2M7.gif)

“TRTL Logo 3d” _A 3d animated gif of the TRTL shell emblem by_ **_vr_nico#3176_**

![]({{ site.baseurl }}/images/0-OSjxwwCGXFs43YQ.png)

**Proton Wallet — Halloween Release!**

“Hey guys, Extra here, the new version of Proton wallet is going to be coming out on Halloween, 10/31 and it has some features I’m very excited about. We’ve implemented a brand new address feature and a search feature, which should make it easier to send transactions and navigate through the wallet. The search feature is pretty nifty; you can search transaction hashes, contact details in your address book, or even for settings you’d like to change, and it will return any results to you in a nicely formatted list. In addition, I’ve found and squashed a few more bugs that result in faster syncing when minimized, and an overall better user experience.

You can grab the newest release at the link below, and please let me know what you think or if you have any feature requests for Proton!

For next month’s release, I’m going to be focusing on adding deterministic subwallet support. This means you’ll be able to generate as many new addresses as you’d like and use them, and be able to restore them all with a single seed. It’’s a feature I’ve wanted to see in a TurtleCoin wallet for a while.

Thanks everybody and stay cool! BD”

**ExtraHash**

[turtlecoin/turtle-wallet-protonYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/turtlecoin/turtle-wallet-proton/releases)

![]({{ site.baseurl }}/images/0I_7xKWtjgHDuacqN.png)

**TonChan**

“On Wednesday the 14th I finally put out an update to TonChan, for 10% of users. If there are no errors discovered then I’ll deploy it to everyone shortly. This update has some big fixes, the major one being a fix where your wallet received a ton of transactions, and you were on Android 9, you may have been unable to open your wallet.

This is caused by only being able to read 1MB of data at once from a single row in the database. This is fixed by just chunking the wallet in the database, and hopefully retroactively fixed by those who have too large wallets by performing chunked reads.

Another big feature is the ability to swap nodes. Now if there’s ever maintenance on the blockchain cache, you’ll still be able to sync your wallet. Furthermore, you can choose a node which is closer to you geographically or potentially under lower load for improved sync speeds.

Finally, I made some tweaks to ensure that the UI is always snappy whether your node is having issues connecting or not.

I’ll not bore you with every single little change made, if you’re interested in that then you can check out the full changelog here: <https://github.com/turtlecoin/turtlecoin-mobile-wallet/releases/tag/v1.0.1>

Let me know if you’re having any issues with the new update. Hope you like it.”

**Zpalm**

[TonChan - TurtleCoin Wallet - Apps on Google PlayEveryone Keep your TurtleCoin secure in a native wallet, where you own your private keys. No more relying on…play.google.com](https://play.google.com/store/apps/details?id=com.tonchan)

![]({{ site.baseurl }}/images/08auD_LWcCylK5Cxo.png)

**GitHub Actions CI/CD**

GitHub has finally released its own CI/CD with some amazing specs. So I decided to try it out and move the entire CI pipeline of TurtleCoin from travis and appveyor to GitHub Actions. This week I have tested the new caching feature to reduce build times significantly. I have also created a PR to use the artifacts produced in these builds for releases and testing purposes..

**rashedmyt**

[upload artifacts to GH Releases and S3 from GH Actions by rashedmyt · Pull Request #920 ·…Following changes have been done in this PR Uploads build artifacts to GH releases (only on release event) and S3 (for…github.com](https://github.com/turtlecoin/turtlecoin/pull/920)

![]({{ site.baseurl }}/images/0sRT9q52pZ8NQszwC.png)

**Low Orbit Turtle Cannon**

Use wallet API to create N wallets, spread some turtlecoins between them, and then spam the transaction pool with pointless transactions between them nodes. Great way to stress test _cough_ DDOS _cough_ your network!? Just a hackathon though, if someone wants to think about it. It could be a bit naughty, sir. Just posting these so you can collect hackathon ideas for people to discuss and use.

**leturt**

**Turtle Tinder**

![]({{ site.baseurl }}/images/0nw-zyoFRXlTeKiux.png)

It’s what happens when two turtles meet under the covers of a blockchain transaction ❤. They spawn new extra special turtles, only for you my friend! They are not turtlecoins but rather virtual turtles, in the spirit of cryptokitties and titties. I could write how it could work here, but the margin is too narrow to contain it. Therefor, just do it your way!?

**leturt**

![Previous page 1 2 Continue reading](https://miro.medium.com/proxy/0*3liQByq9hQBlTTxv)

## **Extra’s Reporter Articles**

Hey everybody, Extra here, reporting on some of the goings on I’ve seen in the past week.

## New Reporter Role

We’ve been having some issues getting enough submissions for the roundup, so we decided to switch up the way we do things a little bit. We came to the conclusion that lots of stuff worth talking about was getting done each week; but these folks weren’t to keen on writing up a few sentences for our blog. So, we created the reporter role on discord. Zpalm, ibmcd and I, and perhaps a few others I am not aware of, will be writing up short reports on cool goings-on we see down in #dev-general and other areas when we see them. This is an attempt to get some more content into the writeup, and also perhaps encourage the authors of these cool projects to come forward and write little bit about them to the community so that all of you guys knopw what is going on. With that being said, here are some of the cool things I’ve seen in the last week or so…

## Mysterious Third Party Wallet Integration

A new face has appeared down in #dev-general asking some techie questions. His name is @zhang, so if you see him around be sure to give a turtley “”hello.”” He’s been working with the turtlecoin-wallet-backend-js on a mysterious-sounding project. We reached out to zhang for comment, and he informed us that he was working on integrating TurtleCoin with his third party wallet application. That sure sounds interesting to me, and we are looking forward to seeing what happens with it! Welcome zhang to the community and good luck with the integration!

It is a pleasure to add turtle to HebeWallet, the first purely anonymous coin for Hebe Wallet.  
We got a lot of help from the turtle community in integrating Turtle in the wallet. Most communities ignore third party development, but we were able to get alot of questions answered very quickly. This saved us alot of time. We will release it in the next version.

[Hebe WalletSupports direct recovery from Hebe，Btc，Ltc，Eth，Etc，Bch，Waves，Doge，Xzc，Nxt，Ardor， Xas…hebe.cc](https://hebe.cc/)

## New Test for the JSON Node List

Ibmcd has been hard at work as usual, and he has a certain talent for setting up cool CI testing. For those that don’t know, we run a list of turtlecoin public nodes on github that other applications can use in order to find active TurtleCoin full nodes for their users here: <https://github.com/turtlecoin/turtlecoin-nodes-json> Up until now, maintainers of that repository have had to manually check to see if a node is online: However, no longer is that the case. IBMCD has written a fully automated check that happens with Travis and will ensure your node is reachable from the internet directly in the CI testing. If you say, open a PR with a dead node, the CI test will fail and you will be automatically notified on the pull request page on github. That’s really neat! Nice job IBMCD. :muscle: :triumph:

## Aneki’s Bootstrap

Aneki has recently updated his bootstrap of the TurtleCoin blockchain for those of you with slow CPUs who want an easy way to get synced. As always, you can find the updated bootstrap at the link below:

**ExtraHash**

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

![]({{ site.baseurl }}/images/0qufUVzyRaMjHNU60.gif)

This week we added two new reporters to a new role called… you guessed it, Reporter! The reporter’s role is to write down cool things that happen during the week that would otherwise not make it into the roundup. Pitch them a few TRTL if you see them being helpful!

Also big thanks to Spookypool who’s starting up a new TurtleCoin pool, we thank you! Best of luck!

**Reporter**: ExtraHash, Zpalmtree

**Service Operator** — Munchiehigh420 Spookypool

Congrats guys!

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- Use matches property in ApiDispatcher regex #862 <https://github.com/turtlecoin/turtlecoin/issues/862>
- Remove no longer relevant asserts #811 <https://github.com/turtlecoin/turtlecoin/issues/811>

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

**“Laptop” by Greywolf**

Editor’s Note: _Picture was submitted but the link was invalid. I assure you it had two beer holders, fold out ash trays, dual flux capacitor and 64 TB of damascus plated DDR12._

![]({{ site.baseurl }}/images/0AMVoxtUv3T7Wz9M9.jpeg)

Dell Latitude E7240 Business Laptop, with Intel Core i7–4600U, 8GB RAM, 256GB SSD, Windows 10 Pro. i attached thick foam (about 2" thick) to the bottom to raise the unit up enough to allow the exiting fan exhaust underneath to flow unimpeded. the Intel HD Graphics 4400 graphics controller no longer mines with any newer software but once contributed to the combined hash rate of the laptop back in early 2018 until the end of last year. i mined my first cryptocurrency with this laptop (TurtleCoin, of course) getting in on the rewards from block 296675\. send me 1MM TRTL and I’ll share my “secret tips and tricks about mining TRTL” greywolf approx 2.5 KH/s with trtl-chukwa on TRTL

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

- MarketCap.cc is the new one stop solution for every crypto trader; developed with one mission in mind: keep crypto stats fake volume free. MarketCap.cc ist the first ever public statistics website that analyzes all trades in realtime across a large number of trusted exchanges in realtime. Combined with out Trading Terminal you will never miss a good trade. MarketCap.cc is still in active development, expect bugs which will be fixed as soon as we find them. [https://marketcap.cc](https://marketcap.cc/)
- Hello. My name is Kevin, owner of SpookyPool.nl. My goal with SpookyPool is to create a great community with fun people and having a nice chat about crypto and other stuff. Having TurtleCoin in my pool since a while ago has been fun. Learned alot of new things and meet alot of new people. I would like to ask u to join the community of SpookyPool by mining TurtleCoin or some other currency! [http://trtl.spookypool.nl](http://trtl.spookypool.nl/)
- Please support the muxdux turtlecoin mining pool — Active Discord with great people, very low pool and tx fees, great hardware infrastructure [https://trtl.muxdux.com](https://trtl.muxdux.com/)

![]({{ site.baseurl }}/images/06qscLdVdJOBw2_uu)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

- Michael Meyers Dont touch my lunchmeat. Or the bread. Or the mayo.
- Japakar pneumonoultramicroscopicsilicovolcanoconiosis
- Japakar Thanks all to the community as always! You guys are great!
- Turtley McTurtleton McDrizzle Hi there!
- Rock Thanks to the reporters and new service operators for entering the fray :)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-november-19-2019/)_._
