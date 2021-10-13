---
layout: "post"
title: "Interview w/ Turtley McTurtleton McDrizzle from ForkMaps.com"
description: "@Turtley McTurtleton McDrizzle Thanks for doing the interview. I wanted to talk today about ForkMaps, and what forking means to the community, and why it’s worth tracking. The forkmaps.com story goes…"
image: "{{ site.baseurl }}/images/1998Z_NwfzTUDuZmlQIEnNQ.png"
date: "2018-10-18T23:31:48.963Z"
---

![]({{ site.baseurl }}/images/1998Z_NwfzTUDuZmlQIEnNQ.png)

forkmaps.com

## RockSteady (TRTL)

@Turtley McTurtleton McDrizzle Thanks for doing the interview. I wanted to talk today about ForkMaps, and what forking means to the community, and why it’s worth tracking.

## Turtley McTurtleton McDrizzle

The forkmaps.com story goes something like this… A couple of months ago, RockSteady said he wished someone would make an updated version of the fork timeline on the CryptoNote Wikipedia page. Turtley McTurtleton looked around a bit, didn’t find anything that was being maintained, and had only one response… “Hold my beer.” “I’m on it.”  
The timing was just right. I was evaluating frontend JS frameworks for an upcoming work project, and rather than writing some contrived “hello world” sample, I used forkmaps as an opportunity to test a handful of frameworks in a real-life scenario.

## RockSteady (TRTL)

That’s really cool. While making forkmaps is there anything that surprised you about all these forks?

Turtley McTurtleton McDrizzle

I found the general friendliness by the CryptoNote community a little surprising. I’ve ventured into many discord servers either looking for project details, or advising someone to restore license headers, and I almost always receive a warm greeting.

RockSteady (TRTL)

Tell us a bit about the tech behind the project and how it all works. I noticed the front end got noticeably faster to load recently. Can you talk about that a bit for some of our nerdier readers?

Turtley McTurtleton McDrizzle

I used Vue.js for the frontend. I wrote it using Vue first, then rewrote it using React, and then messed around with a handful of other frameworks/libraries. I’ve used AngularJS and React quite a bit in the past, and to me, Vue is the perfect marriage of the two.

The site has very few dependencies. I used three Vue packages (base, vue-router, vuex), axios for HTTP requests, and echarts. I didn’t use a CSS framework, so design took me forever, but taught me a lot.

![]({{ site.baseurl }}/images/0B6lNpme1TYgcq1sI.png)

Turtley McTurtleton McDrizzle

To tackle performance, I cleaned up a lot of my JS, replacing a lot of nested functions with array reducers. I added a few CSS transitions to smooth out navigation, added loading indicators (which you should almost never see), and threw in some other UX tricks. Other than the fork map page, my improvements were mostly about perceived performance. You can make something that’s actually very fast, feel slow through clunky UX, and that’s what I’d done with my first attempt.

On the map page, I switched from vis.js to echarts, which is much more UX-friendly.

That was a lot, and I promise I’m almost done.

On the data side, all of the CryptoNote coins live in a separate git repo, as individual coin files to make them easy to manage. Whenever there’s an update, I run a gulp task to combine them into a single json file, which forkmaps.com pulls directly from GitHub. This way, it’s trivial to add additional coin families in the future.

## RockSteady (TRTL)

That’s really cool, what do you plan to add to it next and what kind of helpers are you currently looking for?

## Turtley McTurtleton McDrizzle

Next I’m working on a timeline representation similar to the example you initially showed me. Someone’s working on the 200k TRTL bounty for adding start/end dates to all of the coins as we speak. After that, I want to do max supply, emission curves, primary emission length, and possibly current supply. That one’s been requested a lot, and I think it’ll make an interesting chart. Most coins seem to have a primary emission measured in decades, while Nerva is only three years. I’m always happy to send TRTLs to anyone who contributes data or ideas.

![Jerme404's ForkMaps.com](https://miro.medium.com/max/60/0*VNfMugUC_Ty2ns1H.png?q=20)

![Jerme404's ForkMaps.com](https://miro.medium.com/max/1400/0*VNfMugUC_Ty2ns1H.png)

Jerme404’s ForkMaps.com

RockSteady (TRTL)

That’s great that you’re including the community in this project, and even chipping in bounties for people who are helping out. With so much exposure to all of these different forks, surely you’ve come by some really interesting ones. If you don’t mind, let’s run through a few of the more memorable ones to you: Which fork has the best logo in your opinion — What is the most interesting fork — Which forks do you mine — What’s the worst fork name you’ve encountered — If you made a fantasy fork tomorrow, what would it be called and what would it do?

Turtley McTurtleton McDrizzle

I like logos that don’t look like a coin. Some of my favorites are Boolberry, Alloy, Athena, Lethean, Nerva, TurtleCoin, and Karai (not on my site yet, but the logo is solid). Right now, I think the most interesting fork is Nerva. I’m looking forward to seeing what happens when the supply is exhausted in like 2.5 years, and CPU-only mining is the shit. I only mine Nerva and TurtleCoin. I rent some of my miners on miningrigrentals, and I used that income to buy more TRTL. Worst fork name? How about all of those dumbass XMR forks that happened when Monero switched their PoW algorithm? Actually, Sadomi might be the worst. I really don’t think they thought that one through.  
A fantasy coin for me would be a TRTL fork so I’d always have a reliable codebase and community, and I’d implement a prime sieve PoW component similar to riecoin. I’d call it Turtimus Prime.

![]({{ site.baseurl }}/images/0flW2v38WqiFmvYKu)

## RockSteady (TRTL)

Haha that sounds fun. Whats up with Prime Sieve? tell me about that

## Turtley McTurtleton McDrizzle

So basically, you have an algorithm for finding prime numbers, or prime number patterns. Many projects have chosen to do something “useful” as PoW, at the expense of cryptographic security. But why not both? Add a secondary PoW step that’s relatively easy to perform, does something interesting, and throws another wrench at potential ASICs.

## RockSteady (TRTL)

That’s cool, I think we’ve about got it all covered, is there anything you want to add?

## Turtley McTurtleton McDrizzle

I’m glad you asked!  
Years and years ago, before cryptocurrency was a thing, I had a closet full of crunchers (mining rigs nowadays) working hard on distributed computing projects like folding@home (Team 32!) and BOINC/SETI. Back then, there was no financial incentive to spend lots of money on hardware and electricity, but we did it anyway. Some did it for a cause, some for leaderboard points, but I think most did it for the knowledge and the community.  
I treat crypto projects the same way. At this point in my life, my time is far more valuable than any amount of hardware or hashrate, and there’s a big reason I spend so much of that time with my fellow turtles. And TurtleCoin is the only project I’ve found that really embodies that sense of teamwork and community that the distributed computing scene seems to have lost to crypto over the years.  
So to all my turtle-fam, keep up the good work, and stay turtley!

## RockSteady (TRTL)

Jerme, I’m glad you did this interview, and I’m happy you’re a part of this community! Thanks for everything you do with ForkMaps and otherwise, and I look forward to what you come up with next!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/interview-w-turtley-mcturtleton-mcdrizzle-from-forkmaps-com/)_._
