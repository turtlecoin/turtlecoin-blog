---
layout: "post"
title: "This Week In TurtleCoin (Feb 17 2018)"
description: "The chat grew from 4736 to 6945 turtles this week!"
image: "{{ site.baseurl }}/images/0oHgkGkr5NZDIQV30.png"
date: "2018-02-24T03:33:22.932Z"
---

**The chat grew from 4736 to 6945 turtles this week!**

This past week has been a rager! We survived the 187000 algorithm change, but the battle’s not over- everything’s forksville again on the pools! With that being said, I’ll keep this weekend update brief while we work on a solution so our pool admins can get a nap! As they say, ‘the crazy life of a blockchain never stops’, if you’re the type that is jazzed about witty puns :)

![]({{ site.baseurl }}/images/1zdc3bhE9ABWF_HOV4IV3kg.png)

**Today’s Value, 2SAT — BTC@10782**

- **TurtleCoin on ABC Australia TV?! —** TurtleCoin was featured on a segment on ABC Australia, which was quite the surprise! About a minute in to this video featured on ABC, on the right of the screen you can see TurtleCoin’s logo, just about as big as the Ethereum logo next to it. Funny seeing that! A little premonition.. maybe?  
  **ABC Australia —** <http://www.abc.net.au/btn/story/s4800480.htm>
- **RPC Disclosure —** Our industrious brains on the Turtle Team were working hard last week in disclosing a quite vicious RPC vulnerability, surprisingly still with a lot of bite in 2018, as it was first discovered years ago. The vulnerability allowed an attacker to drain an open wallet as the users surfs the web. MalwareBytes recently interviewed RockSteady about the matter, pending publication.  
  **RPC Disclosure —** <https://medium.com/@turtlecoin/mess-with-the-best-759c1fd230b1>

![]({{ site.baseurl }}/images/1sy-osTD7IvK0Y4EVyPZT_Q.png)

**Aditya’s TurtleCoin Pool Monitor**

- **Aditya’s Pool Monitor —** We have a new contributor who’s currently tearing up the mobile scene with all of his hard work, his name is Adi, and he’s the guy who makes our new Android Pool Monitor! If you’re out and about and you have a cluster of rigs up and mining, you can now check stats from your favorite pools to make sure everything is still moving forward. Great job, Adi!  
  <https://github.com/adigupta13/TRTLMiningPoolObserver><https://play.google.com/store/apps/details?id=ml.fifty9.poolmonitor>
- **TradeSatoshi —** Wallet is finally out of maintenance mode. Thanks to Kim and the team at TradeSatoshi!  
  **TRTL on TradeSatoshi —** [**https://tradesatoshi.com**](https://tradesatoshi.com/)
- **Mnemonic Seeds! —** Our very own ZedPea seized the day and has integrated importing from mnemonic seeds in Simplewallet, which matches the work that Ereptor did on Paper Turtle that enables us to create them. This means instead of using long view and spend keys, you can now regenerate your funds from a phrase of simple words you can write down or remember.  
  **Mnemonic seeds will be in the next release, 0.3.3**

![]({{ site.baseurl }}/images/1NpI5CwXdbWXM8druY8MO6A.jpeg)

Out of the Shell, #2 — Turtle? is interviewed about being our best helper

- **Out of the Shell #1, #2** — Our very own, Gigantomachia, has begun a new TurtleCoin interview series that’s getting pretty popular, called “Out of the Shell” where we pull aside contributors from our community and ask them a little about about what gives their shell a spin :)  
  **Check them out if you haven’t yet!**  
  **#1, Adjoining —** <https://medium.com/@turtlecoin/out-of-the-shell-1-adjoining-aka-ric-from-mexico-a79ad3946b7>  
  **#2, Turtle? —** <https://medium.com/@turtlecoin/out-of-the-shell-2-turtle-d9c3dfdaf6b2>
- **TurtleCoin Core 0.3.2 —**A few changes went in to 0.3.2, and the good news is, this has helped out the exchanges, the bad news is, we’re getting some reports of high volume daemons coming out of sync. This means pool operators are about ready to toss me off a bridge right about now as their chains can get just enough out of sync sometimes to cause problems. We’re working hard on replicating the issue on dev machines so we can narrow down a concrete fix, but in the mean time taking many stabs at possible solutions just in case. As always, we’re optimistic, and this should not affect the overall stability of the network, but it is our first priority and a primary concern to fix this issue. Service operators keep this network moving, often un-thanked! Don’t forget to say thanks to your pool operator, if you see them today.

![]({{ site.baseurl }}/images/0oHgkGkr5NZDIQV30.png)

**Golang, will you be our savior? Circle \[yes\] or \[no\]**

- **Golang, Stability, and the Future** — We’ve been hard at work making reliability and stability improvements to the current codebase, in C++. Some bugs have been easier than others, but the whole way, we’ve been getting closer and closer in familiarity to our code base and its little quirks, and it’s left us wondering what more we can do..  
  Long story short, rather than put too much more duct-tape on the current project, we’ve begun taking a close look at what a complete redesign may look like, starting with a base written in Golang, with performance and security in mind from step one. We officially broke in to teams Thursday and began the process of assessing the Daemon and Simplewallet components of the project. This starts by diagramming from a protocol level what is needed to make these components work from scratch.  
  **I look forward to this project quite a bit, as it will be a fresh start for all of us to create this machine how it was meant to work, from the ground up.**
- **Proposal 001** — A proposal has been made for a solution to fix stuck transactions — be sure to make your opinion heard on this issue if you have any feelings one way or the other.  
  **Proposal for Standardized Mixin, Transaction Size, & Transaction Fees for Large Sends**  
  <https://github.com/turtlecoin/meta/issues/59>
- **Forknote, Call for participation —** Forknote, the project that helped us become TurtleCoin, is looking for development help in integrating Monero into their build software, and as a community, we’re keen on helping those who’ve helped us. Please take a minute to review the details here:  
  <https://github.com/turtlecoin/meta/issues/57>
- **GUI Wallets —** Just in case you weren’t aware, we have a few GUI wallets that are receiving regular updates and lots of love from our community contributors, and if you’re into graphical programs rather than command line, these are right up your alley!  
  **Turtle-wallet is our python GUI wallet**; if you’re into Python or like tinkering, this is the one for you!  
  <https://github.com/turtlecoin/turtle-wallet>  
  **Xamarin-wallet is our windows GUI wallet**; if you just want to unzip a folder and double click an icon to get started, this one is your best bet.  
  <https://github.com/turtlecoin/desktop-xamarin>
- **Wreiner’s Build Script —** This one is more for us nerds, and less for the regular users, but there’s someone named Wreiner in the chat who’s helped us out quite a bit and made a build script that does a few things we were forgetting to do in the Linux builds, which is including static libraries for a few things. If you use Debian to run TurtleCoin, then this one’s for you, my friend!  
  <https://github.com/turtlecoin/turtlecoin/blob/master/build-release.sh>
- **Docs and Wiki —** AC, Bebop, Zed, and a bunch of other industrious Turtles have been working hard on our documentation fragmentation issue lately. We have a lot of guides, but they’re all spread out, so these guys came together to bring you some cool documentation repos for users, devs, and operators. When they are done, these repos will merge, and become our knowledgebase. I hope some day we can be the most well-documented project out there, and these guys are pushing that vision forward every day!  
  <https://github.com/turtlecoin/turtlecoin-wiki><https://github.com/turtlecoin/docs><https://github.com/turtlecoin/turtlecoin/wiki>

## I’m probably missing a few; it’s been a big week! If you’d like your project or update added, please shoot me a line! — RockSteady
