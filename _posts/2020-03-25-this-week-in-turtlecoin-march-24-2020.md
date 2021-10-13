---
layout: "post"
title: "This Week In TurtleCoin (March 24, 2020)"
description: "This week we all came down with a bit of a cough in rapid fashion. In other news, we’re running out of Doritos, please send help. -TurtleCoin Dev Team Video: An 8K hi-resolution Gource diagram of…"
image: "{{ site.baseurl }}/images/0ZkeMv08nSqVlsyIm.png"
date: "2020-03-25T07:02:43.637Z"
---

![]({{ site.baseurl }}/images/0ZkeMv08nSqVlsyIm.png)

_This week we all came down with a bit of a cough in rapid fashion. In other news, we’re running out of Doritos, please send help. -TurtleCoin Dev Team_

**_Video:_** _An 8K hi-resolution Gource diagram of TurtleCoin developer activity in our core software repo from birth until 2020\. Inhale deeply, sit back and turn on some Led Zeppelin or something, it’s pretty cool._

## Developer Updates

This is a place where anybody in our community can submit a post about the TRTL project they’re working on. It’s a great way to attract helpers for your project and show people what to keep an eye out for. We encourage you to show works in progress as well as finished products, as we’re happy to see them all and it shows that we’re an active community.

## TurtleCoin COVID-19 Relief Fund

As a followup to our previous TurtleCoin COVID-19 press release, I’ve been hard at work preparing a stimulus package and the means to distribute it to turtles in need. From the essential workers to the already infected, this bot will guarantee TRTL in your pocket despite the hard times.

![https://media.discordapp.net/attachments/688916582994542682/692217084507324436/unknown.png](https://miro.medium.com/max/40/0*QnDBo7yoVuI8gO55.png?q=20)

![https://media.discordapp.net/attachments/688916582994542682/692217084507324436/unknown.png](https://miro.medium.com/max/1356/0*QnDBo7yoVuI8gO55.png)

The attached image is simply a preview of what to expect. The numbers aren’t final and I’m looking for donations to fund this thing. Consider it a modified rainbot for our times. I’m putting 500k of my own TRTL in to start, but increasing the pot will increase the fun!

shoutouts to moonmoondogo.

**madk bitch.**

## Blockchain import / export files

This week I have been experimenting with importing and exporting blockchain bootstraps. You can currently import the blockchain from the set of .bin files, but as I think I may have mentioned in another update, I’ve been working on removing those, to save hard drive space to store the blockchain.

![]({{ site.baseurl }}/images/0k2kjk60Wpmqgsx6h.gif)

technically this image _is_ block-related..

Since the .bin files will no longer exist to be imported with, I’ve added a way to export the blockchain via the daemon, and subsequently imported again. It will also support exporting ranges of the blockchain, so you could, for example, import blocks 2 million to 2.2 million, if you want to catch up your daemon which is synced to 2 million and not have to download and import the whole chain.

Another avenue I’m interested in exploring is allowing syncing wallets via importing one of these bootstraps. This should be faster to sync than directly downloading blocks from a remote node, as there will be no database latency and no network latency.”

**Zpalm**

[WIP: No longer require .bin files to be stored by zpalmtree · Pull Request #1033 ·…Needs testing. Needs verification of how corruption is handled. Should save a large amount of disk space. May want to…github.com](https://github.com/turtlecoin/turtlecoin/pull/1033)

## TurtleCoin.lol 2020 Visual Brand Update

A few weeks ago we got a suggestion to do a site redesign, and after a short conversation in #dev_marketing we had to agree, things were looking a bit dated. Since then, about a week so far, we’ve redesigned the main site and aren’t showing signs of stopping- we think you’ll note a few differences:

- Instead of a road map or cute story about bebop and rocksteady’s drinking escapades, we now have a dynamic section with links to our most recent blog articles, most recent dev activity, and most recent issues that need helpers on GitHub.  
  We think this is more potent data than what we had. With the dynamic data views we replaced it with we think it will show that we’re active and hope that it gives prospective developers and contributors an easy list for getting started helping us out.
- We’ve decided to pursue a more modern and friendly visual theme than the cryptocurrency-hackery aesthetic we had before (which most of us also really liked). There’s nothing wrong with the look we had, but as we grow and look back, the rough-and-tumble aesthetic of our website very much reflected the state of the core software we had at the time, with all its flaws included.  
  Since that time, we’ve chiseled the TRTL software into a solid peer2peer no-trust-required payments network sporting a new set of washboard abs. To signal that change to the uninitiated users we’re hoping to attract, we’re adopting a more unified and professional look to solidify our commitment to being a great payment network, not just a cryptocurrency.

With the new visual path laid ahead of us, we’re starting next on our Branding Manual PDF as well as our social media assets. Thanks to all the Turtles who contributed to the marketing and branding convo in #dev_marketing that inspired this change.

## TurtleCoin 2020 Presentation Slide Deck

To best support this transition to a more ‘presentable’ face, we’ve gone ahead and made a new slide deck for TurtleCoin presentations which follows the same visual theme as the site. (Any aspiring brand ambassadors out there, feel free to use these to present TurtleCoin to your peers at any clubs or meetups you may have)

The brand new MIT-license-carrying slide deck style mimics the appearance and visual aesthetic of the new website, and presents some basic guidelines for assembling a visually pleasing and cohesive presentation. We’ll include picture previews below, and will provide the templates in PowerPoint, Google Drive, and PDF formats soon for you to make your own presentations at your local hackerspace or university.

![]({{ site.baseurl }}/images/02EFVOgP9CdtLmuxx.png)

![]({{ site.baseurl }}/images/0pGRQLFk7svHK6njT.png)

![]({{ site.baseurl }}/images/0QhJGkN7b6aVzKtYN.png)

![]({{ site.baseurl }}/images/0JTEO7pNx8ebzBCoG.png)

![]({{ site.baseurl }}/images/0KB-MONFIjJwK7JZB.png)

![]({{ site.baseurl }}/images/0To_PznJwRa9ypp8O.png)

## TurtleCoin 2020 Website Preview

In researching the current top 100 currencies on CoinMarketCap, we noticed a consistent visual theme in a lot of the sites. Many of them stopped moving in 2018, about mid-February or March, and their visual first-impressions conveyed that message clearly like a crypto-geocities.

> It became evident that our redesign should clearly communicate one thing- TurtleCoin keeps pushing forward, both during the hard times and the good.
>
> RockSteady

Our new visual theme conveys a welcoming visual appearance of an actual payment network like PayPal or Venmo with less emphasis on buzzwords and concepts that don’t matter. This approach of radical honesty sets us apart from the played out crypto-website trends of abstract-geometry javascript wireframe animations and mountains of jargon. Common frustrations in our research were that around the 40th website or so, it took so long to get past the marketing BS and slow page loads that we just closed the tab and moved on.

If you can’t serve a website that loads in under a second and can’t convey your message in the next 5 seconds, you’re not going to hold the attention of the minds of 2020\*

_\*unless boobs are involved, in which case all bets are off.._

![]({{ site.baseurl }}/images/0YHrFFOPO27GqxmWx.png)

We’ve got a more ‘tangible’ tagline now which says in plain, honest terms what we are, and prompts the user with a button to start a 3 step process to get started with using TurtleCoin.

![]({{ site.baseurl }}/images/070VeurzcUz6VYe-G.png)

The first panel presents familiar icons for a user to choose their operating system and it then downloads the correct software. They’re likely to need help, so in panel 2 we give them an easy list of our social media contact options so while they’re downloading the software they can easily get help or meet peers.

![]({{ site.baseurl }}/images/0rwhLUdOABk340gkE.png)

With the focus on rapid user conversion through providing a fast path to engagement, we’re trying to turn eyeballs into capable hands as fast as possible. Past interactions have led us to believe that the faster we give someone their own ‘piece’ of the community to manage and take leadership of, the more of a chance we have at keeping that person and marching them up through the steps of being a user -> helper -> contributor -> developer.

![]({{ site.baseurl }}/images/0weOjgPwQfneMmqXr.png)

In panel 4, we’ve already been introduced, you’ve likely already started downloading our software and are probably chatting with us in the Discord, so your next question is naturally going to be “whats up with TurtleCoin”. Panel 4 has a list of recent community activity where they can quickly get a glance at the live updated stream of progress to get an idea of what we’re working on and what we’re offering. This is live data, meaning we don’t have to update this, the site does it all on its own. It will never be stale info.  
Also of note: the last section there has technical implementation-level information a business would need to interact with our network or to communicate with our peers. It’s not only normal users and devs reading our site, a lot of exchanges list us without asking us for help, a lot of services do the same for what they build, and frankly they shouldn’t need our help with the amount of effort the community put into documentation that is so good it holds your hand through the entire process of building a web wallet or exchange or other service that needs to connect to our network.

![https://i.imgur.com/s7X3cwe.png](https://miro.medium.com/max/60/0*7FN8Yl6rqUpcm1MS.png?q=20)

![https://i.imgur.com/s7X3cwe.png](https://miro.medium.com/max/1400/0*7FN8Yl6rqUpcm1MS.png)

Sajo8’s awesomely addictive game, CHUKWA’S LABYRINTH!

## Chukwa’s Labyrinth

Hey guys! So you may remember the game I was making, Chukwa’s Labyrinth, from a LONG time ago. I started it last summer! Well, with coronacation going on now, I’ve found time I needed to work on it. The UI has been revamped and I’ve added bigger levels as well new powerups.

Additionally, I’ve integrated TRTL payment, so later on, you will be able to buy some DLC with TRTL through the game itself. Check the “”Buy DLC”” button in the Options screen to see more. Shoutout to ibmc and z for helping me, and to zoidberg for his great trtlapps.io service!

Of course, the entire game is open-source, and you can check it out at the links below. I will be releasing a full beta with 10 levels (albeit no DLC) soon, so you guys can try it out and provide advice for the final product.  
I’ve been working quite a bit for quite a while on this project, and it’s exciting to see it reach near completion, and I hope you guys will enjoy playing it!

**Sajo8**

You can try out my game by downloading it from the following link:

[Sajo8/chukwas-labyrinthYou can't perform that action at this time. You signed in with another tab or window. You signed out in another tab or…github.com](https://github.com/Sajo8/chukwas-labyrinth/releases/tag/v0.2-beta)

Other links:

[Sajo8/chukwas-labyrinthTurtleCoin-themed game where you have to go through a series of mazes in order to reach the treasure Explore the mase…github.com](https://github.com/sajo8/chukwas-labyrinth)

[TRTL Arcade | GamesExplore the Labyrinth and discover the treasure Sajo's first game! A great use of the Godot Engine, Currently under…www.turtlearcade.games](https://www.turtlearcade.games/chukwa.html)

[Sajo8/netlify-expressAn example of how to host an Express.js app on Netlify using serverless-http. See express/server.js for details, or…github.com](https://github.com/Sajo8/netlify-express)

## Good First Issues

Good First Issues are tickets that are marked as ‘easy wins’ for new developers. If you want to be a TurtleCoin Developer, these are great tasks to start with!

- Port raw html to static github site  
  #6 <https://github.com/RocksteadyTC/trtl2020/issues/6>

## Shoutouts & Thanks

This is the place to mention someone in the community who has done something nice or deserves recognition.

RochStetti di Medici Thanks to zpalm and iburnmycd for helping with the situation in #quarantine-general

RockSteady Thanks to Jerme for the bribes financial contribution

> An update on #quarantine-general
>
> Weird things have been happening to the people chatting in this channel. Users are advised to keep a 6 foot distance between themselves and any surfaces in that channel, and to wash your hands before, during, and after shitposting in there. There is a tangible risk, you’ve been warned!! bewaaaaare ooohh spoookyyyyy!!!!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-24-2020/)_._
