---
layout: "post"
title: "This Week In TurtleCoin (Feb 9 2018)"
description: "The chat grew from 4736 to 6032 turtles this week!"
image: "{{ site.baseurl }}/images/1y2d8XIKGg-RPWSCFjEjr0w.png"
date: "2018-02-10T09:39:41.069Z"
---

![]({{ site.baseurl }}/images/042LmH7JSowY-goLR)

**Today’s Value, 4SAT — BTC@8805**

**The chat grew from 4736 to 6032 turtles this week!**

TurtleCoin turns 2 months old today, and to celebrate, we threw a party for our 5000 members. We intended to make it rain turtles in the chat for only one night, but what followed was a 3 day long monsoon of non stop tips. Bebop was the organizer for the party, and I look forward to what he has planned for 25000 members!

- **TradeSatoshi —** We’ve been listed on TradeSatoshi Exchange, and featured as coin of the week. Because of the algorithm upgrade, it’s been a bit of a bumpy road to get them set up, but we’re taking responsibility in finding a solution, while in the mean time TradeSatoshi has been very helpful and patient. **Big thanks to Kim and the team at TradeSatoshi!**  
  **TRTL on TradeSatoshi —** [**https://tradesatoshi.com**](https://tradesatoshi.com/)
- **CoinGecko —** Big shout out to CoinGecko this week for getting not only TurtleCoin but also TradeOgre integrated in record time after users started tweeting up a storm demanding Turtles. Thanks guys, you really work fast!  
  **CoinGecko —** <https://www.coingecko.com/en/coins/turtlecoin>

![]({{ site.baseurl }}/images/0maT6A5R5iDSlztCa)

- **/biz/cord AMA —** Thanks to ChadTrad for inviting Bebop and RockSteady to the /biz/ discord server to hang out for a few hours and answer some informal AMA questions and have beers with the community. We had lots of fun, answered lots of answers, and made some new friends (hey howard!)  
  **/biz/cord AMA —** <https://discord.gg/kp8RaE>  
  **Astronautt Coverage —** <https://www.astronautt.com/q/> **by PrinceTurtle**
- **Delta Crypto Tracker App —** We got added to Delta, so for those of you who need that quick pocket price update for your hoard of shells, you’re in luck!  
  **Delta Crypto Tracker App —** [**https://getdelta.io**](https://getdelta.io/)
- **TurtleCoin Core 0.3.1 —** The new algorithm update designed to discourage botnets and hash rate spikes has proven a bit troublesome, which has caused sync problems at our newest exchange integration, TradeSatoshi.  
  We owe a great thanks to use DiscoTim, and his helper Tom, who have done a magnificent job of pinpointing the issue to daemons that use the `--data-dir` and `--log-file` were experiencing issues calculating network difficulty. They determined that out of everyone who upgraded to 0.3.1, those who ported their legacy chain from 0.2.2 were fine, and those who syncd a fresh chain from 0.3.1 were unable to run successfully for longer periods, causing many orphans and much frustration. This is my mistake, and thanks again to all of our pool operators and bounty participants who have worked patiently and diligently around the clock to get our services back up again.
- **TurtleCoin Core 0.3.1 Bounty —** On the bright side, a chat and github user “DeerTacos” has contributed what they believe to be a fix in a pull request currently being review by our own Napoleon Bonafrog.  
  _“After running the daemon for a while, the wallet could start to throw an ‘Internal node error’. Sometimes the wallet would get stuck like this, and throw it a few times a minute. You’d then have to restart the daemon to get it to work again. I’m pretty sure my pull request has it fixed. Some other guys are running my code as well to make sure my fix works for them too.” — DeerTacos_  
  **_PR —_** <https://github.com/turtlecoin/turtlecoin/pull/53>
- **Facebook Asia —** Chat user and contributor Rybofy bought a Facebook ad targeting the eastern community, thank’s so much Rybofy!!
- **Tom’s Block Explorer —** Tom’s a good dude, and usually the guy to say “I got a server for that” for just about everything. Check out his block explorer and watch a few blocks get assembled live. “_So it looks like an edge case was missed in the difficulty upgrade, existing daemon block caches would be upgraded if present, but new instances would sync from 0 as if the change was already applied. Sorry about this, fix in the works_”-Tom  
  **blocks.turtle.link —** [**https://blocks.turtle.link**](https://blocks.turtle.link/)
- **BitcoinTalk Announcement —**Thanks to Adjoining, and Napoleon and the rest of the turtles who urged us along and helped us launch our BitcoinTalk ANN.  
  **BitcoinTalk —** <https://bitcointalk.org/index.php?topic=2872287>

![]({{ site.baseurl }}/images/1zUcwBajVGkzfNfKyBcj_Mw.png)

**MoonMoonDogo’s Turtle Rain Bot in the #Raindance channel**

- **Turtle Rain Bot —** Chat user MoonMoonDogo made a really popular bot that accepts TRTL, and makes it “rain” on chat users who try to catch it by responding to the bot with the right emoji. It’s been such a big hit! Thanks Moon!  
  **rain-turtle —** <https://github.com/turtlecoin/rain-turtle>
- **Brand Guidelines** —Turtle contributors from the #dev_marketing room put together a really nice brand guidelines book that rivals a lot of professional brands out there, and it’s really helped the community come up with a cohesive look for the project. Outstanding work, you guys!  
  **Brand Guidelines PDF —** <https://github.com/turtlecoin/brand/blob/master/TurtleCoin_Brand_Manual.pdf>
- **TurtleCoin GUI Wallet —** Our python GUI wallet got some upgrades to the way payment ID’s and RPC works, so if you were able to send money to an exchange this week successfully, drop those turtles a thank you note and tell them thank you for the great work!  
  **Turtle Wallet —** <https://github.com/turtlecoin/turtle-wallet>

![]({{ site.baseurl }}/images/1y2d8XIKGg-RPWSCFjEjr0w.png)

**Ereptor’s Turtle Map, currently on**[ **TurtleCoin.lol**](https://turtlecoin.lol/)

- **Ereptor’s Turtle-Map! —** This is by far the coolest thing to replace particles.js since the invention of the sparkle GIF. I can’t wait for people to see our new website with the turtle map replacing the old particle animation, because it shows you just how many people there are on our network and how spread out we are. Thank you to all of you, and especially the one guy on that tiny island in the middle of the North Pacific Ocean operating a node; you’re the real MVP!  
  **TurtleCoin.lol website — https://turtlecoin.lol**
- **turtlecoin-walletd-rpc-js —** This is a really important project being worked on, and even though it started out just as a fun common sense thing to Bebop, it ended up being used in some pretty important integrations. Thanks Bebop!  
  **rpc-js —** <https://github.com/turtlecoin/turtlecoin-walletd-rpc-js>

![]({{ site.baseurl }}/images/1vYO9oeWiKkM5DjNGs96umQ.png)

**Play Turtle Trouble —** <http://gigatank3000.com/turtle-trouble/>

- **GT3000 —**After the success of last week’s Turtle Trouble, GT3000 couldn’t be stopped as he got right back in the saddle for his next installment in the Turtle Arcade. _“On the heels of Turtle Trouble we’re not resting and going into our latest project, as of now it’s untitled but we have a working premise. “In the dark future of 2084, Turtles are a prized commodity that have displaced the USD as fiat currency. However their printing is tightly controlled by the ILLUMINATI until you showed up. From your TURTLESTATION, print Turtles and grow in power. Topple the ILLUMINATI’s control of Turtles and save the world.” We hope to have a working prototype soon and get it into your hands!” Thanks GT3000!!! Love what you’re doing with the story line!_  
  **_Play Turtle Trouble —_** <http://gigatank3000.com/turtle-trouble/>
- **Kinjo’s Turtle Runner Game —** Kinjo says **_“_**_We have started development on a new TurtleCoin video game with a native TurtleCoin store. The primary concept involves playing as a turtle who is slowly moving forward. Jump around and hide in your shell to avoid obstacles. But if you get hit, it’s game over! And best of all you can play it in browser whilst you mine!”_  
  **Beginning Dev Soon —** <http://github.com/turtlecoin/turtle-runner-game>  
  **Kinjo’s GitHub —** <https://github.com/AntonStrickland>  
  **CptCrunchy’s GitHub —** [**www.github.com/cptcrunchy**](http://www.github.com/cptcrunchy)  
  **Giselle’s GitHub —** <https://github.com/cupcakeBullet>
- **Docs, Docs, Docs! —** ZedPea has been really putting in work as far as organizing docs and guides from the community for all types of useful things, but the biggest hit so far is the guide on catching rain!  
  **Docs Repo —** <https://github.com/turtlecoin/docs>
- **Wiki, Wiki, Wiki! —** Bebop and a few others have a work-in-progress on porting docs from the docs repository over to our wiki, and he’s looking for helpers last I heard, so if you’d like to contribute a guide and get your name on the wiki, this is your chance!  
  **Wiki —** <https://github.com/turtlecoin/turtlecoin-wiki>
- **Paper-turtle** — Paper Turtle got an upgrade this week from the guys in #dev_general who made a mnemonic decoder to match the mnemonic scheme on our paper wallets. Thanks MoonMoonDogo for the decoder, and Ereptor for fixing the paper wallet to provide mnemonics as well as a decoder.  
  **paper-turtle —** <https://github.com/turtlecoin/paper-turtle/commits/master>  
  **turtle-decoder —** <https://github.com/MoonMoonDogo/paper-turtle>

![]({{ site.baseurl }}/images/1-19lrUzu08Y3uGA0CrK4Qw.png)

Follow [@crypto_rocky](https://twitter.com/crypto_rocky)

- **Rocky’s Big Giveaway! —** Rocky’s wildly popular Twitter giveaway was a massive success, and was totally a generous way to introduce some new turtles to the community!  
  Three lucky new turtles got 50,000 TRTL as prize for their participation. Great job you all! Thanks to bdougiYO, TayoHatch, and redsandisk for joining the community!  
  **Twitter —** <https://twitter.com/crypto_rocky/status/961922259714748416>
- **Turtle Memes on the Twitters —** Twitter just got a lot cooler this week with the introduction of April O’neills very own personal twitter account, which dispenses all the shelly-meme goodness from our chat’s #meme channel, service up hot copy pasta for all your shelling needs! Post one today!  
  **Follow TRTLMemes on Twitter —** <https://twitter.com/trtlmemes>  
  **TRTLMemes on GitHub —** <https://github.com/turtlecoin/turtle-meme-tweeter>
- **Turtle Xamarin GUI Wallet —** This is probably our most popular wallet, and this week it got some updates which should have automatically been pulled in by your wallet, so if you have run it this week, you’re all set! There’s some unavoidable hiccups with the wallet while we transition to our new difficulty algorithm next week, so post issues if needed, but keep in mind it’s only temporary as the network works out the new algo switch.  
  **Xamarin GUI Wallet —** <https://github.com/turtlecoin/desktop-xamarin/releases/download/1.0.6609.42743/TurtleWallet_1.0.6609.42743.zip>
- **Wreiner’s AUR Repository —** Chat user and code contributor Wreiner has done all of us neckbears a solid and made an AUR repository for those of us who are cooler than our friends. You can install with your favorite manager by pulling in **turtlecoin-git**  
  _“For our Arch Linux users we created AUR packages to install with their preferred AUR helper, a bin and a git-based build”-Wreiner_  
  **_AUR —_** <https://aur.archlinux.org/packages/turtlecoin-bin/>

# And now a message from our sponsors…

**Need some sweet Merch to show off to others that you are a TRTL Coin miner?**

**This is the first run of TRTL Coin approved die cut stickers for purchase off of the TRTL Coinwebsite.**

**($1.50 minimum or $0.00035 TRTL Coins, Both are accepted)**

![]({{ site.baseurl }}/images/0gSNjS67_766IA7aG.png)

For stickers, contact CptCrunch in the Discord chat

![]({{ site.baseurl }}/images/0aLQYh7-0fMJRdfgQ.png)

For stickers, contact CptCrunch in the Discord chat

## **I’m falling asleep at the keyboard here, so I want to wish everyone a great weekend, you’ve earned it! If your project didn’t get an update and you’d like to be included, let me or Bebop know about it and we’ll get you all fixed up. — RockSteady**

## **Cowabunga dudes!**
