---
layout: "post"
title: "This Week In TurtleCoin (July 2)"
description: "This week we learned how to talk trash one pixel at a time, started building dapps, got drunk and forgot to write the Roundup, and more!"
image: "{{ site.baseurl }}/images/0ghXGNjYmiHlgCgl-"
date: "2018-07-03T14:29:29.997Z"
---

## This week we learned how to talk trash one pixel at a time, started building dapps, got drunk and forgot to write the Roundup, and more!

[Follow](https://medium.com/m/signin?actionUrl=https%3A%2F%2Fmedium.com%2F_%2Fsubscribe%2Fuser%2F4317739209c6%2F737f02ade221&operation=register&redirect=https%3A%2F%2Fcryptocurrencyhub.io%2Fthis-week-in-turtlecoin-july-2-737f02ade221&user=TurtleCoin&userId=4317739209c6&source=post_page-4317739209c6----737f02ade221---------------------follow_byline-----------)

[](https://medium.com/m/signin?actionUrl=%2F_%2Fapi%2Fsubscriptions%2Fnewsletters%2F17580acb5efe&operation=register&redirect=https%3A%2F%2Fcryptocurrencyhub.io%2Fthis-week-in-turtlecoin-july-2-737f02ade221&newsletterV3=4317739209c6&newsletterV3Id=17580acb5efe&user=TurtleCoin&userId=4317739209c6&source=post_page-----737f02ade221---------------------subscribe_user-----------)

[Jul 2, 2018](https://cryptocurrencyhub.io/this-week-in-turtlecoin-july-2-737f02ade221?source=post_page-----737f02ade221--------------------------------) · 8 min read

[](https://medium.com/m/signin?actionUrl=https%3A%2F%2Fmedium.com%2F_%2Fbookmark%2Fp%2F737f02ade221&operation=register&redirect=https%3A%2F%2Fcryptocurrencyhub.io%2Fthis-week-in-turtlecoin-july-2-737f02ade221&source=post_actions_header--------------------------bookmark_preview-----------)

![]({{ site.baseurl }}/images/0ghXGNjYmiHlgCgl-)

**TurtleCoin OneClickMiner**

**TurtleCoin OneClickMiner —**_“I’m back online and the OneClickMiner for TurtleCoin is still alive! The code finally reached a point where I was able to commit it to the repo. New features include support for xmrig, dynamic or manual pool selection with several options and cleaner code under the surface. Before filing the new release (which will bundle the most recent miners) I need some testers for the current code to find and correct the last bugs. (Look for the correct folder structure!) Check out the GitHub repo and don’t hesitate to ping me on discord! See you!”_ **_—_ EncryptedUnicorn#7915**

[turtlecoin/one-click-minerone-click-miner - One click miner GUI for xmr-stak to specifically mine the Turtlecoingithub.com](https://github.com/turtlecoin/one-click-miner)

**zedwallet —** “Added a few improvements to zedwallet this week — quite a lot was changed so I’ll list the interesting ones.

![]({{ site.baseurl }}/images/1VtG2NiQPDPgEXgrGxpT2YA.png)

Address Book

- **Address Book —** An address book has been added — this lets you save an address and an optional payment ID to a friendly name, to send to later. This is handy for sending to often used addresses, such as your tipjar.

![]({{ site.baseurl }}/images/1CfaOec5IWI7OhU9BdlP3qQ.png)

Help Command

![]({{ site.baseurl }}/images/1xcbSawdl6Z42tU6pYkYZIA.png)

Advanced Commands

# Trending Cryptocurrency Hub Articles:

> [1\. The Bitcoin Bubble Explained to a Couple of Four-Year Old Twins](https://cryptocurrencyhub.io/the-bitcoin-bubble-explained-to-a-couple-of-four-year-old-twins-95b6f86e3b90)
>
> [2\. Ten Steps On How To Properly Research A Cryptocurrency (Before Investing)](https://cryptocurrencyhub.io/10-steps-on-how-to-properly-research-a-cryptocurrency-before-investing-f10c31ef91e1)
>
> [3\. Win 200 ETH in New Tournaments!](https://cryptocurrencyhub.io/win-200-eth-in-new-tournaments-320bb0b69d3)

- **Slight UI Revamp —** You can now enter commands either by their name, or by their ‘number’, listed next to the command name. Furthermore, commands have been split into two types, basic ones, which are displayed when you type ‘help’, and advanced ones, which are displayed when you type ‘advanced’. This helps us add lots of cool commands without making it overwhelming to new users who just want to view their balance and transfer, etc.
- **A change_password command was added —** If for some reason you want to change your password, you can now do it without having to reimport your wallet from the beginning.
- **Readline support —(** Mac + Linux only) Thanks to @mrrovot for adding this — This allows zedwallet to behave more like a typical Linux command line application. It allows tab completion of commands, using up/down arrow to select previous commands entered, along with some other nice features. Unfortunately, GNU Readline is pretty tricky to get working on Windows, so this is only for the unix users :(
- **Timeout on status command —** You might have noticed a new `status`command in zedwallet recently. This is pretty handy, but occasionally, TurtleCoind would hang whilst responding, so the command would never complete. A timeout was added to prevent this from locking up your wallet. Thanks to all the contributors who have helped out with PR’s and feedback :) Like the sound of some of these improvements? You can build from source to start using them now! :)” — Zpalm

[turtlecoin/turtlecoin/zedwalletturtlecoin - TurtleCoin is a private, fast, and easy way to send money to friends and businesses!github.com](https://github.com/turtlecoin/turtlecoin/tree/development/src/zedwallet)

![]({{ site.baseurl }}/images/0AOyvwmyUc5NL0n15.png)

**XMRig Stats Aggregator**

**XMRig Stats Aggregator — _“_**_Simple python REST server written with Flask that scans the local network for workers running XMRig (hope to include xmr-stak as well in the future) on a given port. The server can then be queried (GET) to return statistics on all workers found, and a rescan can be triggered via POST. This hopefully could be used as an easy-to-use backend to create a dashboard/UI to monitor all your workers within your network.”_ **_—_ auto-joe**

![]({{ site.baseurl }}/images/1TGe9aMlUaxRfL3hapqSCuQ.png)

**Gladiator Bot**

**Gladiator Bot —** _“Gladiator Bot allows users of Turtlecoin’s Discord to engage in player vs player battles. Start with 100hp and beat the life out of your opponent! Recently, potions were introduced in and shortly after buffed. Potions are a purchasable item, offered to heal you during battle. The cost of the potions helps to sustain the bots tipjar and allow battle prizes to be awarded. The most recent addition is the chance of a potion critically healing. Currently, potions heal for 30hp. However, there is a 5% chance that your potion will be critical and heal you for a staggering 100hp! The prize is now tied directly to Turtacus’s tipjar — meaning for every prize, you will be awarded 0.01% of his total overall balance. The more he holds, the more you win! The tournament will be taking a change this week. With the reduced match prize, the weekly prize needed to be more appealing. So as of next week, the overall prize will be 20,000 TRTL. 1st place will take 50% (10,000), 2nd place will take 35% (6,500) and 3rd place will take 15% (3,500). Turtacus now has a website which shows not only the top 10 leaderboard but also a full stats board showing every player. This is located at_ [_http://gladiator-bot.infinityws.co.uk_](http://gladiator-bot.infinityws.co.uk/) _and will improve over time as I get better with CSS. I am working on implementing stats — Strength, Agility and Defense which will alter how combat turns out. However, this is causing me many headaches and is taking longer to implement than I’d hoped. However, it WILL happen! Good luck in the colosseum — It’s every Turtle for themselves now!”_ **_— Rynem_**

[TurtacusWebsiteEdit descriptiongladiator-bot.infinityws.co.uk](http://gladiator-bot.infinityws.co.uk/)

[Rynemgar/Gladiator-BotContribute to Gladiator-Bot development by creating an account on GitHub.www.github.com](http://www.github.com/rynemgar/gladiator-bot)

![]({{ site.baseurl }}/images/01AWJfnPcCC5iB7pp.png)

**Nest wallet**

**Nest wallet —** _“A new version of Nest wallet will be released in a few days with backup and import from a 25 words seed. That version will also include fusion transactions, which should solve the issues that some users have for sending large transactions. The first version of Nest was released only 3 months ago, and Nest has already been downloaded 9300 times. Help us reach the 10K downloads!”_ **— Jon — Nest**

[turtlecoin/turtle-wallet-goturtle-wallet-go - A universal gui wallet for TurtleCoingithub.com](https://github.com/turtlecoin/turtle-wallet-go/releases/latest)

![]({{ site.baseurl }}/images/1HjvUqoCqC_RH2zmEIJDooA.png)

**Swanson Rig**

**Swanson Rig —**_“\_Swanson is running on hiveOS and is pulling an average hash rate of 10.46 kH/s on turtle.imhard4.men. I managed to get about \~2.24 kH/s extra with overclocking the cards by editing the ROM files and flashing them (very easy with hiveOS, would recommend anyone checking them out!). However this significantly increased power consumption (60%), thus I will most likely be running the overclocked settings only at night when it’s much cooler :)_”\_ **— Fexra**

- **Frame** (1x Aluminum Open Air GPU Mining Frame)
- **Power Switch** (2x Electop PC Switch Cable LED Light)
- **RAM** (1x Ballistix Sport LT 4GB DDR4 2400)
- **Risers** (6x PCI-E 16X to 1x, 6pin)
- **Motherboard** (1x Gigabyte GA-H110-D3A)
- **SSD** (1x Kingston SSD 0400 120GB)
- **CPU** (1x Intel Celeron G3930)
- **Power Supply** (1x Corsair RM1000x)
- **GPU** (3x MSI RX 480 8GB)
- **GPU** (2x Powercolor RX 480 8GB)
- **Cooling Fan** (5x) — still waiting

![]({{ site.baseurl }}/images/17-Sx_ayMI-y92veBjrCfGg.png)

**Spreading Turtlecoin awareness**

**Spreading Turtlecoin awareness! —** _“Special thanks to Browns1964Champs for supplying the marketplace with TurtleCoin stickers. The stickers are very nice quality and perfect bumper stickers or for spreading around the community. No better way to spread awareness while supporting your favorite cryptocurrency!” — Xaz_

![]({{ site.baseurl }}/images/0xxBbJKKShTmi0Nmb.png)

**TRTL Pixels —** “It’s live, we can now draw things pixel by pixel with our precious TRTL! (Rock please write something better here for me ❤)” **— Canti**

![]({{ site.baseurl }}/images/0CBeYyKw1vrMmVl7Q.png)

This is the aftermath of just _part_ of an automated picture upload on the chain. That’s almost 4000 tx’s in the pool waiting to go in the next block!

“TRTL Pixels is pretty cool! If you have a bitchin’ bald spot and a fond memory of Million Dollar Homepage, then you probably already know where I’m going with this! You can spend 1 TRTL per pixel to fill in any kind of picture you want, anonymously, one pixel at a time! Orrr… if your beard is strong you might automate it!” **— Rock “Just look into it” Steady**

[TRTL PixelsONETRTLEQUALSONEPIXELwww.trtlpixels.com](http://www.trtlpixels.com/)

![]({{ site.baseurl }}/images/05Wx_UfHp9vajJeIi.jpg)

![]({{ site.baseurl }}/images/0r9Pi46CHIBLHCJnO.jpg)

![]({{ site.baseurl }}/images/0YqetSp_RM7VTFSMm.jpg)

TurtleCoin Snail Races

**TurtleCoin Snail Races —** _“Today, 6/30, we have added to our snail pool approximately 30 tadpoles and 30 minnows as well as some azolla and pond scum. This will help to create a good environment for the snails to live. We are blessed to have the #snails channel on trtl network where updates and discussion about these upcoming races may be held. As of right now we hope to be up and racing by the end of July! Keep on being awesome :)”_ **_— Roger Robers_**

# Shoutouts from the Community

**Cryptoroach#5655** — turtle roach

**cvstn —** welcome back crappy :)

**Khem Boi —** Shout out to my mama for believing in me and the entire turtle coin community for making crypto great again

**Khem Boi —** \*suspicious bear stare\*

**Not Shortok —** Hey @everyone, Shortok is now live on <https://www.twitch.tv/shortok> ! Go check it out and represent TurtleCoin in the chat!

**tjwmagic —** Turtle Miners Club is a premier mining pool for anyone wanting to mine! We are small, but steadily growing. Everyone is welcome to join! NEWS: We just release a new website featuring individual worker statics and a Top 10 Miner list!

**Rynem —** Shout out to Fexra for not swearing whilst putting his rig together! You cost me man, but I salute you!

**ar-x —** Thanks to @Jihadist, @CaptainMeatloaf for finally wrapping up the Russian translations.

**ar-x —** Thanks to @D4rkGh05t, @Mineirofox for shipping the Portuguese translations.

**Rogerrogers —** Shout out to all the people that make the TurtleCoin community so great ❤

**Xkasl —** When android wallet

[![](https://miro.medium.com/max/60/1*Wt2auqISiEAOZxJ-I7brDQ.png?q=20)![](https://miro.medium.com/max/510/1*Wt2auqISiEAOZxJ-I7brDQ.png)](https://docs.google.com/forms/d/1apzYQHO6Qdt7ng5yUPFO_LG4ABWFBwUl6FSRo25zozY/edit)
