---
layout: "post"
title: "This Week in TurtleCoin (April 2, 2019)"
description: "This week our biggest April fool’s joke was saved for the peddlers of ASIC and FPGA mining hardware. RIP, till next time, old friends. Quick update on the EDU side! Fexra and I got a wild hair up our…"
image: "{{ site.baseurl }}/images/01sg2U5g68HFD2Pmh.png"
date: "2019-04-03T05:01:15.932Z"
---

![]({{ site.baseurl }}/images/01sg2U5g68HFD2Pmh.png)

_This week our biggest April fool’s joke was saved for the peddlers of ASIC and FPGA mining hardware. RIP, till next time, old friends._

## Developer Updates

![]({{ site.baseurl }}/images/0MFK_Mv5iNeRIquK-)

TurtleEDU is now open for enrollment! New classes coming!

**TurtleEDU — The First Semester!**

Quick update on the EDU side! Fexra and I got a wild hair up our butts and replaced the entire OpenEDX system with a new e-learning suite that has been an absolute pleasure to use. It’s called LearnPress, and is much more suited for what we’re doing. We were able to port over the **TurtleCoin 101 — Intro to TurtleCoin** class during a lunch break, and Fexra had it styled a few hours later. Everything’s working, students are rolling through it much faster and without any issues like we had on EdX with weird activation problems you can read about in old roundups.  
So it works, and students are passing- what’s next? Right now Sajo’s putting together the Github 101 class where we use some simple non-code-based examples to teach normal users the single most important tool we use in TurtleCoin development, Git. Git helps you save your progress as you go so that you can roll back when things break and go back to the last time it was working, your work never gets lost and is always available to use. It’s a great asset to us and the first step in being a TRTL Dev is to learn Git! Keep your eyes peeled and be sure to enroll in the TurtleCoin 101 class we have up now!Sajo’s class is up next for contributors, and soon after will be the dev class!

TurtleEDU is an important part of the ecosystem for us because it helps us take people who are completely new to this stuff and turn them into competent users, and then turn those users into capable developers who help push the project (and themselves) forward to new heights! Join us, we’ll teach you everything we know if you’ll net us. — Professor Rock

[TurtleEDUOnline Courses for Blockchain Users and Devs.edu.turtlecoin.lol](https://edu.turtlecoin.lol/)

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products. To submit your link, click this link_ <https://docs.google.com/forms/d/e/1FAIpQLSdTs4nDSKai2fPpCnuT0WXzutCuJQk7nFlFqYCgmBlz4DEM7Q/viewform>

![]({{ site.baseurl }}/images/04dNLCEvqKhl0kaZc.png)

**This is Dumb Derek. He skimmed the roundup article and didn’t know about the upgrade, now he just wants to panic-sell on TO and nothing works. Don’t be like Dumb Derek.**

**TurtleCoin Algo Upgrade — “Chukwa” Argon2id based**

**Blog Article:** <https://blog.turtlecoin.lol/archives/the-quest-for-decentralized-proof-of-work/>  
**Branch:** <https://github.com/turtlecoin/turtlecoin/tree/codename_chukwa>  
**Benchmark Test Results:** [turtlecoin/turtlecoin#716](https://github.com/turtlecoin/turtlecoin/issues/716)  
**Speadsheet Form:** <https://docs.google.com/spreadsheets/d/1TJVqJsDCswgdTvtkhJfrg09rQAV9KifUKC2KDg0WkMc/edit#gid=1912293181>

> Currently, our implementation of Chukwa is kind of like that time Dick Cheney went ASIC hunting and accidentally shot his GPU friend in the face. We’re doing what we can to bring a GPU miner to the community before the upgrade kicks in but for the time being Chukwa is CPU only.
>
> RockSteady Jenkins, ‘6-pack Proverbs’, 2nd ed. 1996, O’Reilly Pub.

![]({{ site.baseurl }}/images/0K4vUkYSJ0Y6rHjr0.png)

XMRig via Termux on Android -

**XMRig via Termux on Android**

Discord fellow afterconnery#5552 put together a quick guide for running XMRig on Android via Termux. It is the 3rd way to run a miner on mobile. Few of us have given it a go or plan to. On my Pixel C was able to get 800H/s and on a slower MediaTek MT6737T 1.5GHz 4 core I get 400H/s. It’s probably not a great idea to run this 24/7, just a bit of fun. Join us in the mining channel on discord and post up your results — [http://chat.turtlecoin.lol](http://chat.turtlecoin.lol/) — **SoreGums**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/wiki/Using-Termux)

![]({{ site.baseurl }}/images/0ZDglXa3iTTWXPmB1.png)

I posted it — rock

![]({{ site.baseurl }}/images/00g3CzZlBRYfw0ADb.jpg)

(Codename) Cthulhu’s Revenge

**\[Cthulhu’s Revenge\]**

In between everything else I have going on, I’m working on tackling building new pool software from scratch. This package, currently under development is affectionately referred to as “Cthulhu’s Revenge”. So far, I’ve abstracted stratum communication, blockchain monitoring, hash validation, and a few other dependency pieces that are required for proper pool operation. I’m not quite ready to publish anything on GH yet, but rest assured, as soon as I am, you’ll see it in #dev_general and in the roundup. — **IBMCD**

![]({{ site.baseurl }}/images/0R6ZpJGjkTxO2U0Uh.png)

Display Unlock Time for Incoming Transfers in Zedwallet++

**Display Unlock Time for Incoming Transfers in Zedwallet++**

The Display Unlock Time feature allows zedwallet-beta users to see how long a transaction is locked for when unlockTime is used through the Wallet API.  
**Some fun backstory:**  
I decided to grab a “Good First Issue” from TurtleCoin’s GitHub, and went to work on implementing it into Catalyst (a TurtleCoin fork); as I soon learned, I had to merge a plethora of upstream updates that had been made since Catalyst’s launch, just to be able to test the code I was working on out (great learning experience in-and-of-itself). Once I got Catalyst up to speed, I got to learn about TurtleCoin’s Wallet API features and utilize them to test things out. After getting the hang of things (and after locking some Catalyst up for 1000 years), I made a PR to TurtleCoin to implement the changes. @zpalmtree reviewed my work and suggested changes, I would work on it more, and recommit for it to be reviewed again, with @iburnmycd monitoring the progress and cheering us on. Finally, after working through some of the nuances of the unlockTime feature, like whether it was handled as a block or a Unix time, and smoothing up the formatting to be in sync with zedwallet’s current style, @zpalmtree finally merged the changes to TurtleCoin’s development branch. The experience left me inspired to continue working on improvements for our networks, there’s still so much to do! Much love, TurtleCoin community. — **oddbox (dirtybits on Github)**

[turtlecoin/turtlecoinTurtleCoin is a private, fast, and easy way to send money to friends and businesses! - turtlecoin/turtlecoingithub.com](https://github.com/turtlecoin/turtlecoin/blob/daad2dab3af24acc257f002ee8f7b8099598a3ce/src/zedwallet%2B%2B/CommandImplementations.cpp#L423)

> Big thanks to Oddbox for being the first community contributor to help us out with a Good First Issue! For those of you who don’t know, Good First Issues are easy-wins that are specially marked in our repository for new devs to get an easy entry into our codebase and “TRTL Dev” on your resume. And who doesn’t want a hot pink name in Discord?!
>
> RockSteady, Janitorial Mogul @ TurtleCoin

![]({{ site.baseurl }}/images/0L_3Chwr7_3UOjX3M.png)

Freenode IRC Presence!

**Freenode IRC Presence!**

TurtleCoin now maintains an official presence on Freenode, the IRC network for free and open-source projects! We have linked our Freenode #turtlecoin and #turtlecoin-dev channels to our Discord #general and #dev_general channels, respectively. Come check it out! Thank you to iburnmycd for the bot that makes this possible! **— Thinkpol**

[Kiwi IRCEdit descriptionkiwiirc.com](https://kiwiirc.com/client/irc.freenode.net/?nick=TurtleFan%7C?#turtlecoin)

![Team Chat](https://miro.medium.com/max/60/0*-duaShVE1LSgRpPT.png?q=20)

![Team Chat](https://miro.medium.com/max/1400/0*-duaShVE1LSgRpPT.png)

<https://xkcd.com/1782/>

![Related image](https://miro.medium.com/max/60/0*d0DZEoP8dCdQrBR4.png?q=20)

![Related image](https://miro.medium.com/max/1400/0*d0DZEoP8dCdQrBR4.png)

TonChan Mobile Wallet \[pictured\]

**TonChan Android Mobile Wallet**

Not much to report again. Added a pull to refresh, and refresh on reopening wallet from background for the coin price, as the automatic refresh was basically never getting hit (every hour, provided the wallet was in the foreground).  
I’m aware scanning QR codes is broken in the current version, it will be fixed in the next version. Meanwhile I’ve been trying to finally track down what is causing all the crashes, and I think I have a good way to reproduce it, but am not sure how to fix just yet.  
Reminder that if you have a feature you’d like to see, make a request on the GitHub, and I’ll see what I can do. (Or make a pull request yourself ;) **— Zpalm**

[TonChan - TurtleCoin Wallet - Apps on Google PlayKeep your TurtleCoin secure in a native wallet, where you own your private keys. No more relying on centralized…play.google.com](https://play.google.com/store/apps/details?id=com.tonchan&hl=en_US)

![]({{ site.baseurl }}/images/0RJ6Qi94zb7h9xSch.png)

:comfy:

## **Small News For Small Eyes**

- **Shouts out to OddBox and Professor L** who gained Developer role this week for their contributions to TRTL code repos.
- **TurtleCoin China AMA went well —**  
  <https://github.com/turtlecoin/meta/issues/139>
- **/r/GPUMining AMA also going well —**  
  <https://www.reddit.com/r/gpumining/comments/b72mqs/turtlecoin_ama/>
- **Nobody’s crosslinked** our super-contentious-pow-upgrade (ironic working titles are ironic) github meta thread to the other ongoing PoW cold war threads going on right now, so that’s a plus. Stop by if you like while it’s still civil and quiet.  
  <https://github.com/turtlecoin/meta/issues/141>  
  <https://github.com/turtlecoin/meta/issues/74>
- Some exchanges added us this week, so if that’s your thing you can probably figure it out on Twitter.
- Our 2019 set of TRTL Discord Emojis are already being seen in the wild. No known vaccinations are present at this time.
- #ultranote — added to communities in Discord
- TurtleCoin Core software now has 51 Core Contributors on Github. We want to make it official, but we don’t know which pocket to hang our green bandanas out of.

![]({{ site.baseurl }}/images/07Y9vyXnWZREAlPOl.jpg)

In this picture, a young market-talker sits, verklempt, smeared in the shame of his actions.

## [Good First Issues](https://github.com/turtlecoin/turtlecoin/issues/712)

_Want to be a TRTL Dev? We’ve made a list of our easiest challenges. When your code is merged, you get the dev role :)_

- Support Blockchain cache API in Nigel  
  <https://github.com/turtlecoin/turtlecoin/issues/712>
- Prune Spent Inputs from WalletBackend[ https://github.com/turtlecoin/turtlecoin/issues/708](https://github.com/turtlecoin/turtlecoin/issues/708)
- Daemon+WalletBackend timestamp adjustments  
  <https://github.com/turtlecoin/turtlecoin/issues/704>

![]({{ site.baseurl }}/images/0Fxiwuob0PxYTSUAm)

Morpheus made this :)

## Rig Of The Week — Greywolf “Rig1”

Each week we will post one of the rigs posted to “Rig of the Week”, a new segment that MrLahaye came up with that’s really getting some good engagement. To submit your rig, fill out this form and we’ll submit one a week till we run out. <https://goo.gl/forms/GkDSoP3fERBWm8aJ2>

![]({{ site.baseurl }}/images/0_RxRVzZQUKpoHAyl)

![]({{ site.baseurl }}/images/0Qdm_1sJRhenE26dI)

![]({{ site.baseurl }}/images/0tAryHOnOSGZcGPfj)

**Name**: Greywolf’s mining rig “Rig1”

**mobo**: MSI Z270-A PRO  
**CPU**: Intel Core i7–7700K  
**RAM**: 8GB (4GBx2) DDR4 PC4–19200  
**PSU**: EVGA SuperNOVA 80+ Platinum 1200W  
**GPU**: (x4) XFX Radeon RX580 8GB  
**PCI-e adapters**: Rebbic VER009S

This is the first rig that I built, circa mid-April 2018\. I fabricated a frame with 1/2" aluminum angle bars, 4 wood slats across the bottom, and a wood support beam to stabilize the GPU’s. I drilled holes on the rear rail and tapped them, to accept standard case thumbscrews, for securing the GPU’s. I started with 1 GPU, and added another every few weeks until there were 5\. The motherboard is supported by 6 standard brass standoffs, double stacked, for more clearance under the board. I added a standard mobo speaker, an on/off switch, and a USB 3.0 extension cable attached to the rear, to give easy USB access from the front.

The original motherboard onboard NIC went bad about 2 months ago. The original rig had 5 RX580 GPU’s and a Celeron CPU with a low profile fan (pending the addition of a 6th GPU). When the NIC went out, I swapped the motherboard with an identical one (but different CPU) that I had been using for testing purposes. Because of the displacement of the large cooling fan for the Core i7 CPU, two GPU spaces (3 & 4) on the frame were sacrificed, and now the rig runs only 4 GPU’s, but has a beefier CPU.

**What are your secret tips and tricks about mining TRTL?**  
don’t panic, ask for help, don’t quit

**What is the hashrate of this rig?**  
Masari CPU mining 650 H/s TurtleCoin GPU mining 0 8250 1 6200 2 6200 3 5240 T \~25900 H/s Highest (since 3–16–19): 37596.5 H/s

Bounties!

Bounties are a great way to get things done. Tell us what you want and how much TRTL you’d pay to see it happen and we’ll post it in the roundup for you and see who bites!

- 1000 TRTL — I need windows and mac binaries for my fork of turtlecoin please. @Monster(QPSA)
- 100,000 TRTL — I am offering a Bounty of 100k TRTL to implement TRTL with Trust Wallet!, TrustWallet started accepting more coins for integration recently and I think could be a great form of exposure and additional option for all turtle users. Here is the submission form: [https://github.com/TrustWallet/wallet-core/issues/new?template=new_blockchain.md&title=Add+support+for ](https://github.com/TrustWallet/wallet-core/issues/new?template=new_blockchain.md&title=Add+support+for)and some technical details: <https://github.com/TrustWallet/wallet-core/wiki/Adding-Support-for-a-New-Blockchain>" Mrrovot / Turtle Max
- 10,000 TRTL — Write a guide on mining TRTL on an iOS phone with the app XMR Miner. Must be modeled after existing guides, I can give a hand wherever needed! Sajo8
- 200–700 TRTL per fix — Help correct information or fix broken links in the turtlecoin docs! Bounty depends on information fixed, feel free to contact me for more info Sajo8

![]({{ site.baseurl }}/images/07yD39HanQo01Gp-K.gif)

Submitted by TenaciousTurtle

## Free TRTL Advertising

Do you have a pool or service that runs TRTL? Tell us about it! Advertise here for free every week!

- Merged Mining Turtle + Loki — HashVault.pro [https://turtle.hashvault.pro](https://turtle.hashvault.pro/)
- TRTL man! :) Dice, Blackjack, and 3 other games I dont understand yet! <https://bc.game/>

![]({{ site.baseurl }}/images/013sOJ-mRTlpzv79T)

Submitted by Coco

## Shoutouts & Thanks

_This is the perfect place to thank the people who help you or make things that you like using!_

- Sups — Thank you to Ksupremex for the videos you keep sending in, really helping the community learn the basics of crypto mining and setup, Loved the last video of XMR-stak. It’s great to see how you are following us on our journey, and helping others as you go.
- Ksmith1532#4898 — I wanna give a shout out to @zpalmtree#1337 — for helping fix my miner set up and got me turtle mining again.
- Sierra — Alien stop being so depressing you fucking angsty teenager
- cwappywules — please dont forget me
- Queethan — Sajo, I love you! :t_kissy:
- Cison — Discotim and CodIsAFish, sorry I ddos’d your mining pools.
- zpalm — im eating crisps they’re tasty
- Anonymous — Thank you to zpalmtree and iburnmycd for spending so much of their free time thinking about and working on TurtleCoin.

![]({{ site.baseurl }}/images/0LOgAUs3h75V8H6jU.gif)

Pictured: Peyton from Github handling the dirty work

## Dunce of the Week

_We decided to make a segment on the back page of the roundup to laugh at highlight projects that go further than just a search-and-replace to remove the TurtleCoin License from their forks. This hurts all of us & without that license, we couldn’t have shared TRTL with you._

![]({{ site.baseurl }}/images/0plxHgYGT35MDkpJh.png)

This week’s dunce is ZumPay and their wise ZumDevs, who ignored both TRTL Dev’s and Github’s request to restore the license. The lengths they went to in obscuring the licenses in the code was comical, even going so far as to keep operating as if nothing was wrong even after receiving the polite requests to restore the licenses.

The sweet irony in all of this is that Github responded by acknowledging the violation on April Fool’s Day and taking action the day after.

_At TurtleCoin we encourage the forking and re-use of our code, and usually we’ll even help you to do it properly, however, the first section in the_ [_TRTL Forking Guide_](https://turtlecoin.github.io/fork) _is to respect the license! Without this license, none of this would be possible, and this one simple request allows us to provide you with the software and support our communities need. Thanks for your help!_

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-2-2019/)_._
