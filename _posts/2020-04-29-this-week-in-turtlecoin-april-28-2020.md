---
layout: "post"
title: "This Week In TurtleCoin (April 28, 2020)"
description: "This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye…"
image: "{{ site.baseurl }}/images/0STTS1jSxzPmslN0n.gif"
date: "2020-04-29T06:07:48.136Z"
---

![]({{ site.baseurl }}/images/0STTS1jSxzPmslN0n.gif)

[Contributed to the TRTL subreddit by **u/wisc**lom91](https://trtl.reddit.com/)

## Developer Updates

_This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community._

![]({{ site.baseurl }}/images/0wAjOcXYXCUNQni6p)

turtle.army explorer

## **turtle.army Block Explorer**

Hey guys. I’ve made a new block explorer, just for fun. This one utilizes the excellent turtlecoin-utils library to scrape the blockchain from the daemon and stores it in an sqlite database.

**Yes we are going to run sqlite on a web app, and we’re going to like it.**

It’s still syncing now but maybe in a week or so it’ll get there (lol). I’m considering launching a full suite of TurtleCoin related tools on [https://turtle.army](https://turtle.army/) for the community to use. Anyways, check it out and let me know if you have any suggestions (or pitch a hand and help!)

**ExtraHash**

[turtle.armyTurtle army. 'nuff said.'turtle.army](https://turtle.army/)

![]({{ site.baseurl }}/images/01pROZV4MkAIjVBUM)

Have you seen the new website yet?

## **Add translation feature to TRTL2020 Website**

Hi Turtles!,  
Today I decided to try and port the new Turtlecoin website from html to Jekyll so we can add translations, it took a few hours but it is done and fully working!.

**I am also offering a bounty of 500 TRTL for every translation submitted.**

The site is very clean and lean and only has about 3 sentences to translate, it’ll probably take you a few mins.  
Checkout the repo to see instructions on how to submit your translation and @me on the chat when you do the PR so I send you the trtl

Special thanks to Rock for the help and @Sythe❤#9999 for trying to do it before me and giving the inspiration.

**@Turtle Max#3183**

[turtlecoin/trtl2020To submit or propose changes to turtlecoin.lol, submit a pull request to this repository. This project uses Jekyll to…github.com](https://github.com/turtlecoin/trtl2020)

![]({{ site.baseurl }}/images/0MSqveXe1yzDjDFpv.gif)

## **Brazilian Portuguese translation**

This project intends to translate the Turtle 2020 website into Brazilian Portuguese (for this, proofreaders are required for the translation, allowing it to be approved by the community) and thus integrate people from Brazil and Portugal into the project.

**D4rkGh0st/MrLupus (Discord) and D4rkGh05t (Github)**

[Brazilian Portuguese translation by D4rkGh05t · Pull Request #2 · turtlecoin/trtl2020GitHub is home to over 40 million developers working together to host and review code, manage projects, and build…github.com](https://github.com/turtlecoin/trtl2020/pull/2)

![]({{ site.baseurl }}/images/0J5Rm6D28D26YgUTU)

## Karai Website

I did some work on the marketing page for Karai.io. At the moment we don’t have a whole lot of content, and a lot of that is due to me spending most of my free time after work coding on go-karai, the Golang Karai implementation.

Eventually I’d like to get either github wiki’s working or some other documentation style website set up to share code snippets and API notes for Karai like we do with TRTL stuff and then link to that from the marketing page when someone clicks dev-related links.

Some of you asked to help out, so I’ll be putting this website up at <https://github.com/turtlecoin/karai-website> if anybody wants to help out or make modifications.

**RockSteady**

<https://github.com/turtlecoin/karai-website>

## Karai REST API & Ephemeral Metadata

![]({{ site.baseurl }}/images/0MZGboBCX6QX9-eiM.gif)

**REST-API:** I added a REST API to the go-karai client as part of the pointer process. That doesn’t mean a whole lot if you aren’t familiar with the terms, but what it does is provides an endpoint so that when someone finds a Karai pointer transaction on the TRTL chain, they ping the endpoint and receive a peer ID from the endpoint. That peer ID then helps you get connected to the peer swarm, kinda like the way a bit-torrent magnet link works.

**Ephemeral Metadata:** While we’re on the topic of headers and addresses and such, much work this weekend was put into the scheme by which we tell transactions how they’re ordered and what other connections they’re linked to. The ephemeral metadata field is a non-hashed field, which means transactions while in-formation have a degree of malleability with regard to their positioning in the graph, hence the descriptor ‘ephemeral’. This process is achieved by non-hashed ephemeral metadata fields that exist in several forms:

- **the milestone ephemeral data** — A milestone that is -1 from the existing milestone tip will index the peer participants and subgraphs it has transactions for. This speeds up syncing and allows a short path to syncing just the transactions belonging to you.
- **the wave tip ephemeral data** — One step down from milestone transactions are Wave Tip transactions, which are the first transactions in a listen interval who hold the transaction positional metadata for the subgraph below them.
- **transaction ephemeral data** — This metadata stores the answers to such questions as — who is my parent, who is my neighbor, who is my wave tip, what milestone are we on?

![]({{ site.baseurl }}/images/0ecaLwAzUMZ9E7RYZ.gif)

If some of this sounds kinda weird to you, it’s okay, it’s weird to me too and I’m mainly the guy building it. In short what we’re building is different from something like a blockchain where each block has a block before it and a block after. Karai doesn’t have blocks, all transactions stand on their own, and they can have neighbor transactions linked above, below, and to the left and right, which forms a fractal shape (Karai is a directed acyclic graph).

On its own it sounds like a nerdy thing to get excited about, but it’s a step up from where we are with TurtleCoin, Ethereum, Bitcoin, Monero and other networks where downloading and replaying every single transactions regardless of which ones are yours is the norm. Time will tell.

![]({{ site.baseurl }}/images/0hyWI7HaEb5XVCTV3.png)

## Karai Transaction Store on IPFS

Last week I built a function that takes all of the JSON object transactions in the graph folder and puts them all on IPFS and reports the content ID hashes back to you. I was able to ID 1,000,000 transactions quickly but it was not as fast as I’d liked.

That got me thinking.. How much really needs to happen to these transactions while they’re in-formation (this is what I’m calling the state where the transactions are still being interlinked by the coordinator node) that can’t wait until after the listen interval has concluded?  
I think what I learned from my experience is that I should batch the transaction objects somehow and address them in chunks to make the process faster, and that this process of addressing and pinning the transactions should happen after the formation of the transactions has settled, because otherwise it’s just doing too much at once.

Regardless, the test was a success! This coming week I’ll be spending my free time after work and during lunch checking out the various graph-visualization libraries out there to work out some type of explorer-like representation of the transaction waves. I hope I come up with something cool, I ran across a lot of great examples for directed flow graphs.

## go-karai terminal client for Windows/MacOS

With the help of Rashed, we got the build pipeline created with binaries generated for every release of go-karai on Github. We generated a few test releases (sorry for the noise if you subscribe to updates) and everything compiles as expected. Currently we’re having two issues I need you guys to help me with.

- I use a lot of color in the terminal interface for Karai, it works on Linux just fine, and in Windows it looks fine if you use GitBash or Mingw64 as your terminal, however \`\\033&1;33mIt looks like\\033&0;90mthis \\033&1;33mfor everyone else if they use powershell or windows cmd. Those color codes don’t get interpreted correctly. I tried a few options, and unfortunately could not get it working. If anybody wants to give ANSI 8 bit terminal color in windows a shot, by my guest
- MacOS is compiled, however I’m a brainlet and have never, to this day, got MacOS running in VirtualBox, and don’t own any MacOS hardware. If any of you run whatever the accepted ‘current stable’ version of MacOS is out there, please give go-karai compiled binaries a shot and let me know if you see color at all. Just run ./go-karai and hit enter a few times and if the text is white and green or something similar, it worked. Thanks!

**Rock**

[turtlecoin/go-karaiLaunch Karai in Linux & MacOS Launch Karai in Windows go-karai.exe Type menu to view a list of functions. Functions…github.com](https://github.com/turtlecoin/go-karai)

![]({{ site.baseurl }}/images/0ze9CqRcy7N3eAMtt.gif)

## TurtleCoin Vanity Address Generator (usage tips)

Last week I was shootin the shit with our resident cubist and expert in anything related to colored-squares, Professor L, and was talking about generating vanity addresses for TurtleCoin.

What the hell is a vanity address, you might ask. Because you’re a strong man and vanity is for puffs who wear skirts and lipstick right? WELL. Let me tell you, it’s pretty fucking cool and actually +10’s your manliness with a cool wallet address like TRTLv1**rock**iQcRbC5TB5VAKgVdr3sXqxN8r1q89JKNB5ZJgQYNjoanZgrGiLUaRKLUZXf8FSCgoaudiHwPZVcAqH1Y4QnjC2puE

The vanity address generator has actually been in our repos since the wee early days of TurtleCoin, written by one of the earliest botmasters, MoonMoonDoggo, who also wrote the Rain Bot (or roach bot depending how you felt about it). The generator was written in a compiled language called ‘Nim’ which allegedly is pretty cool according to the sadists who practice that type of witchcraft. I guess it never got the attention it deserved, and when I was reminded of it, I wanted to generate some addresses.

[turtlecoin/turtle-vanitygenThis repository contains Nim wrappers over a few of the cryptonote cryptographic primitives and some address handling…github.com](https://github.com/turtlecoin/turtle-vanitygen)

As I downloaded the source code and sought out to compile it, I ran into a big snag. When I say that Nim is some type of voodoo sorcery, I mean the error this thing shat out into my terminal was so cryptic and arcane, I felt like the compiler had just thrown a glove on the ground at my feet like “I fucking dare you, nerd \*compiler puffs chest\*”. I tried and tried, couldn’t even google my way out of a paper sack that night, but there was a clue. Professor L said that it compiled successfully on a version much lower than the one I had, like comparing 0.17.2 to 1.2.0 or something.

[Nim Programming LanguageThe Nim programming language is a concise, fast programming language that compiles to C, C++ and JavaScript.nim-lang.org](https://nim-lang.org/)

**If you run into these crazy errors, I found the solution. Use a tool called ChooseNim and downgrade to version 0.17.2**

[cloned2k16/niManWARNING: BETA release so don't expect it to work bugless .. and is it still just intented to be used on Windows ...github.com](https://github.com/cloned2k16/niMan)

Also another note, you might be tempted into thinking, “hey what if I open 8 of these windows and do it 8x as fast”, it’s not going to work like you think it will. As Zpalm pointed out, it’s already seeing how many cores you have and running accordingly, and you’ll notice if you run `htop` while it's going it's using 100% of each core until it finds an address that conforms to the prefix you gave it.

It takes only a few minutes to find a prefix with ‘rock’ in it, but so far haven’t been able to get ‘rocksteady’, it is exponentially more difficult with each letter you add. Let us know if you generate anything cool!

**Rock**

## Moving Up!

It’s always good to be recognized! These are the people who gained new roles in the community this week!

**Core Contributor**: LeoCuvee#1481

**Developer**: Turtle Max#3183, LeoCuvee#1481, Buggles#5389

**Contributor**: Alien#5919, Savon#6826

**PR Guerilla**: Kinjo#5916

![]({{ site.baseurl }}/images/0ggNR5M7gaNKOLUe4)

**Mining RigOZ v001** by **Yurii**

## Rig Of The Week

Do you have a TRTL mining rig you want to show off? Tell us about it!

**Rig Description**: x5 RX550 2GB, modded bios, downvolt, 355W on CHUKWA  
**Secrets**: “Just keep mining lol :)”

**Hashrate**: 140 KH\\s on CHUKWA

## Free Advertising

This is a spot to spam anything TurtleCoin related that you would like to advertise, it’s free to put an ad in the roundup.

Sync faster with bootstrap powered by bot.tips. Bootstrap data is regularly updated. [https://trtl-data-dir.bot.tips](https://trtl-data-dir.bot.tips/)

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

**Madk** Shoutouts to mc.evilma.id — the unofficial Minecraft server of turtlecoin. **greywolf** thanks much to zerouan and brätövenhürt for the lively DJ talk show while hosting karaoke **zerouan** thanks yall for supporting vision street wear, lilly meraviglia and not eat any pineapple pizzas **dsanon** shout out to rock for all the hard work on karai! :DD

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-april-28-2020/)_._
