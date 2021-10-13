---
layout: "post"
title: "(aka Zach from England)"
description: "Welcome to the third installment of Out of the Shell, a series of interviews with the developers, designers, and doers behind TurtleCoin. This is @gigantomachia and I’ll be your host. Any open-source…"
image: "{{ site.baseurl }}/images/0w8GAZcgg2VZvGccJ.jpeg"
date: "2018-08-28T22:50:52.649Z"
---

![]({{ site.baseurl }}/images/0w8GAZcgg2VZvGccJ.jpeg)

_Welcome to the third installment of Out of the Shell, a series of interviews with the developers, designers, and doers behind TurtleCoin. This is @gigantomachia and I’ll be your host._

Any open-source crypto project is only as strong as the developers behind it. Though only three months old, TurtleCoin’s developer community has demonstrated that it’s among the most active. CoinGecko, which uses various metrics to rank cryptocurrencies and other cryptoassets to help investors gauge their value, currently [ranks TurtleCoin 64th out of 131,392 coins on the list of coins with the strongest developer community](https://www.coingecko.com/en?sort_by=developer_score) (measured by number of stars, merged pull requests, new commits, etc., on GitHub). That places it above even Bitcoin Cash, which CoinGecko ranks 82nd on the list.

One of the developers contributing to TurtleCoin’s stellar ranking is @Zpalmtree, who so far has roughly 70 commits to [TurtleCoin’s various GitHub repos](https://github.com/turtlecoin). I chatted with @Zpalmtree about his background, how he came to join the TurtleCoin community, what projects he’s currently working on, and how others can contribute. Enjoy.

> **Tips welcome:** TRTLuxvBFVNSxovAp3c9C8h8dUttA4sP8hHELDQJXsQZ7JcKfnn3sLkUPGQgQBkvvhXFfAErUqmf52BzyqFaHhEHicRNLnXYfRj (Gigantomachia)

**How did you first learn about TurtleCoin?**  
I saw a thread about it on 4chan /biz/. Funnily enough, I actually saw the very first thread about TurtleCoin and posted in it a bit, but it was pretty late and forgot about it in the morning. A month or so later I saw another thread, and it looked pretty fun, so I gave the software a download. I didn’t realize I had posted in the original thread until someone linked to it and I read through and realized some of the posts were mine!

**What initially drew you to the coin? What was it about those posts that enticed you to comment and then later download the software?**  
My memory isn’t great, but if I remember correctly it was someone saying that you could mine thousands in a day. I imagine most miners have seen their balances slowly tick up with fractions of a coin, and whilst it may be worth the same either way, having TRTL flow into your wallet in the thousands is a lot more fun. Sure enough, when I woke up the next day, I already had 60,000 TRTL received from one night of mining.

**How long have you been involved in crypto?**  
I’ve been aware of crypto having lurked on /g/ for many years, but I never actually got into it until autumn 2017, when I started mining on a gaming PC when I wasn’t using it. It seemed pretty fun, but I never really sent much of it, what with the high fees and lack of people to send it to really. This is the first crypto I’ve got into the community and been having fun sending tons of small amounts to everyone. It’s great fun to see someone tip you and it to appear in your wallet in a matter of seconds.

**What did you first start mining on the gaming PC?**  
I think it was Ethereum actually. I had recently sold my 480 after the prices shot up from the Ethereum boom, and bought a 1070 with the proceeds, before they too shot up. I then started delving into the whattomine charts, finding out the best coins for my card, which is always a fun way to learn about more alt currencies by trying out their wallets and mining the most profitable ones. Of course, what with crypto being so volatile, you end up with tens of wallets installed and constantly having to swap between them. I then started mining on miningpoolhub for a few months, which auto swaps between the most profitable coins, until I started just mining TRTL full-time.

**What’s your background? Sounds like you know your way around computers. Do you work or are you a student?**  
I’m a student, in my final year of a computer science degree, and am looking forward to getting a job writing software, though my recent experience with TRTL has made me perhaps look towards getting a job developing something blocdkchain related. It’s a fun field to be in with some very interesting tech being developed.

**How long you been coding? Any special areas of focus?**  
I’ve only been programming since I was 17, so not that long. I’m a big fan of Haskell, a functional programming language, and I’m happy to write anything if it’s in that! I like exploring niche programming languages and always looking for a way to use fancy language features to write more concise code. Shoutout to @hai!

**What’s been your contribution to the TurtleCoin community thus far? What projects have you worked on?**  
I think my first contribution was a typo fix! I just saw something in the wallet, which was spelt wrong, so I made a quick edit on the GitHub to fix it, and it was in the code shortly after. Then, after growing a bit more used to the software, I started hanging around the #help channel, and trying to help out the newbies with some common errors. Big thanks to [@Turtle?](https://medium.com/@turtlecoin/out-of-the-shell-2-turtle-d9c3dfdaf6b2) who is constantly in there helping. I’m not sure if the dude ever sleeps. I thought it might help to compile some of the common issues into an FAQ, and now Bebop is doing some good work on the wiki to make it nice and presentable to users, so they can quickly find answers to their queries.

Next, I started looking more into the simplewallet code, a simple fix was changing the checkpoint message to yellow, as a few people thought they were done when they hit there, when it’s just a conformation of valid progress. Then I made a command, view_tx_outputs, which takes a hash and verifies which outputs belong to you, which is handy if your wallet is messing up but the blockchain is working fine. I also added an outgoing_transfers command to match the incoming_transfers command. Finally, I added mnemonic seed support to the wallet, which I think is pretty cool. It’s pretty easy to add features to simplewallet, so please, if anyone notices something missing, let us know or jump in and fix it yourself!

Finally, I setup a few quick scripts to allow the TurtleCoin project to be automatically built every time someone makes a commit or a pull request, on Windows, Mac, and Linux. This is pretty handy to check that we don’t break the build for people on other platforms.

**What’s your favorite pizza?**  
A nice, thin based, spicy meat feast.

**Any particular TurtleCoin projects or initiatives you’re working on right now where the reader can help? Any request for the reader or community, or opportunities for people to get involved if they want?**  
Right now I’m looking at stuck transactions. I’ve isolated the code which returns stuck transactions to the sender, and it’s a bit buggy. We also want to modify simplewallet to not let people send transactions that will get stuck in the first place.

We want to work on making the user-facing software as easy to use as possible, so it’s very easy for people to just download the software and get mining or sending TRTL. The GUI wallet is a great step towards this — thanks @therealcrypt! — but it’s also got a few bugs which are a bit frustrating. This is written in C# which is pretty friendly for newer users to jump in and start modifying the code of — please check the GitHub issues out if you’d like to help out with that.

**C# Wallet —** <https://github.com/turtlecoin/desktop-xamarin>

**Wallet Issues —** <https://github.com/turtlecoin/desktop-xamarin/issues>

The GitHub issues are great ways to find out what needs fixing in the code, and some fixes are as simple as a one-line change. There’s also the meta forum, where people can suggest direction for the project, or potential changes to the software. This is yet another good way to find things you can help out with.

**Meta Forum —** [**http://meta.turtlecoin.lol**](http://meta.turtlecoin.lol/)

We’re also considering rewriting the main codebase in Golang — so if you’re interested in that, please let us know in #dev_general! Speaking of that — lurking in all the dev channels is a great way to tell what’s going on and what other people are working on.

**#Dev_General —** <https://discord.gg/4hJTfEW>

If you’re not a programmer, but still want to get involved — no worries! We constantly have new users coming in, so hanging out in the #help and #mining channels and fixing newbies’ issues is a great way to improve the coin’s adoption. Furthermore, if you’ve got experience in art, graphics, advertising, writing, or anything like that, the #dev_marketing channel is all about making cool things to spread the word of TRTL, articles, posters, or even just posting about TRTL on websites like reddit or 4chan. Finally — TurtleCoin is meant to be a fun coin — so make some cool memes to spread!

**#Help —** <https://discord.gg/4Mg3XBp>

**#Mining —** <https://discord.gg/9uCeDd7>

**#Dev_Marketing —** <https://discord.gg/T3hJGGq>

**When you’re not in class, studying, or hanging out in the TurtleCoin discord, what do you like to do for fun?**  
Playing video games with friends, watching anime and tv series, and reading the latest tech- and programming-related news. I also played my first game of DnD yesterday — very fun!

**Mining some serious coin is what initially drew you to TurtleCoin. What’s made you stick around?**  
The thing that sets TurtleCoin apart from other cryptos for me is the community. It’s so easy to get involved, talk to the devs, look at what other folks are working on, and chat with some like-minded folks. It’s the first project where I’ve been able to easily get tons of my code into the codebase. Before this, I had only made a few tiny pull requests, both one-line fixes.

**Where do you see TurtleCoin going?**

I see TurtleCoin being similar to Doge in that it’s a bit of a meme coin, fun to tip other people with, but whilst Doge is very similar to BTC tech wise, Turtle has nice privacy features, lots of active development, and some interesting plans for the future. Above all it’s a community coin, and I think it has a good place as an introduction to cryptocurrencies for new users, with a friendly community, and an easy coin for new devs to contribute to. I’d love to see more new miners and developers getting involved and having some fun using TRTL!

> **Tips welcome:** TRTLv2Fyavy8CXG8BPEbNeCHFZ1fuDCYCZ3vW5H5LXN4K2M2MHUpTENip9bbavpHvvPwb4NDkBWrNgURAd5DB38FHXWZyoBh4wW (Zpalmtree)

_A note from RockSteady:_

_Zach, Thank you for giving us your time and attention, you’ve really been blazing a trail since you got here and the work you’ve contributed has really helped push this project along. You’re a pleasure to work with, and an important part of this community; we’re happy to have you!_

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/out-of-the-shell-3-zpalmtree-aka-zach-from-england/)_._
