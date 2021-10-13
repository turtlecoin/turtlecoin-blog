---
layout: "post"
title: "From Newbie to Core Contributor w/ ExtraHash"
description: "It’s been a while since we’ve interviewed a member of the team and as we just added a new Core Contributor last week it just felt right to pick back up on the article series. Enjoy! ExtraHash, thanks…"
image: "{{ site.baseurl }}/images/0K2sizKo8cO2TXutl.png"
date: "2019-10-10T21:34:22.759Z"
---

![]({{ site.baseurl }}/images/0K2sizKo8cO2TXutl.png)

![]({{ site.baseurl }}/images/0OS2U9SPxw5nUPIlK)

Here, you can see the knuckles lifting gently off the ground as a user becomes a dev

**It’s been a while since we’ve interviewed a member of the team and as we just added a new Core Contributor last week it just felt right to pick back up on the article series. Enjoy!**

ExtraHash, thanks for taking this interview! You’ve been in the TRTL community for a few years now, and over this time we’ve watched you grow from a normal user to the developer of our default GUI wallet, and now a core dev, in fact! At the end of this interview, I hope the readers get to know you and your projects as well as the rest of us have, and maybe if we’re lucky it will bring people a little bit closer to one of the people that makes the tools they use daily.

So to take it from the top, how did you find TRTL? Do you remember what brought you here initially?

_I found TRTL very early on, within the first month of launch, through a thread someone had posted (where else) on /biz/. It was my first foray into getting involved into a fledgling coin, and let’s just say I didn’t really know what I was getting into. In fact, at the time, I had very little background knowledge of blockchain in general. It was a great experience, and before long I was up to speed on alot of basic blockhain concepts due to the helpful and educational nature of the community._

How long would you say you were a regular user before you got the idea you wanted to be a dev? What was it that made that change?

_I didn’t decide to take steps toward becoming a developer until I had already been in the community as a regular user for a bit over a year, sometime in February 2019\. I’d say there were two major events that spurred my transformation:_

_The first event was a video that you actually posted in_ **_#general_**_, a movie on open source software and Linux called Revolution OS. It really struck a chord with me. Watching that video made me realize what open source actually was: it’s more than just opening your source code for others to inspect, it’s a revolution and community movement based around allowing others to use and modify software and change it as they see fit. This understanding was eye opening for me, and gave me a bit of a different perspective on TurtleCoin and our community._

![]({{ site.baseurl }}/images/0q_tFq8MvJL8B_RYP)

dark mode

![]({{ site.baseurl }}/images/0sztLFBBszV0DUrc-)

light mode

_The second event was the event that actually spurred me to start writing code. Madk had a bot in the market server that was able to give statistics on the network and market: price, hashrate, and so on. He made some changes to the bot that I did not like. So, instead of asking madk to revert the changes, I set out to write my own bot to take its place. That bot became my first ever coding project, and is still running in the market server to this day._

That’s cool, and I’m not sure many people knew that about you. What brought you from doing a chat bot to wanting to design the now default GUI wallet for TRTL?

_The chatbot was written in JavaScript, which I had some (but not much) experience with before, mostly simple scripts on web pages and things like that. I set out to learn as much about JavaScript as I could, thinking it would be best for me to at least become competent with one language before attempting to learn others. There were a few other projects in between which I used to further hone my JS skills, but soon I began to want to contribute back to the TurtleCoin community in a meaningful way._

_At this point, I was also following TurtleCoin’s development very closely, and one thing really piqued my interest: walletbackend-js. Zpalm had written a really nicely done native JavaScript wallet backend implementation, but no-one was yet developing a new wallet with it. Also, the current GUI wallet was fairly clunky and seemed to be abandoned by the developer. I saw a good opportunity to actually start a project that could improve the end user’s experience with using the network, and from that came Proton, my baby and GUI wallet which i’ve crafted for the community._

![]({{ site.baseurl }}/images/0hEK8eVZ1BY_vsMEI)

What does walletbackend-js do for you, or I guess, for Proton?

_Walletbackend-js provides a way to interface with a wallet and the network in native JavaScript, which allows you to do things like write a wallet application or turtle-powered web application. It can run in a lot of places, including directly in a browser. With the old electron-based GUI wallet, there was always some “lag” to the user experience because it was just a graphical front-end wrapping the turtle-service executable. Proton, however, is a 100% native JS application, with no messy child processes._

Is there a vision behind what you’re trying to create? Has becoming the default GUI wallet changed how you feel about the trajectory of Proton?

_Well, to be honest, the intention was always to become the default GUI wallet. Eventually I’d like to add multi-coin support for some of the other bigger coins, I think it’d be neat to have a fully open source client-side multi-coin wallet. However, for now, I’m just focused on improving Proton and making it the best possible experience for users on the TurtleCoin network. If anyone would like to see specific features implemented, please feel free to make an issue on the GitHub page with the feature request._

![]({{ site.baseurl }}/images/05cLenBsYmvN2jfIu.png)

Shows you node fee info too, which is handy

What are some features you’re working on currently that we will be seeing soon that maybe some aspiring developers reading this can help with? Do you have any Good First Issues?

_I’m currently working on a search function to search any information locally in the wallet. It’ll match contacts in the new address-book that will be releasing next version, as well as hashes stored within the wallet such as tx hashes and payment IDs._

_The issue list is looking rather slim at the moment, but I am having one issue with a module called react-select I’m using on the send page for the address input: you can’t access the context menu to paste via mouse click because the real input width seems to automatically resize based on input size. This would probably be a good one to try and tackle._

For anybody who’s reading this who may want to help, can you touch briefly on the different parts of the tech stack that Proton makes use of? It uses nodejs, what else?

_Sure. At its root, yes, it’s a nodejs application. It’s also making use of electron, a framework for developing with web-based technologies on the desktop, and react, a front-end framework for web applications. It’s also making use of redux, react router, and webpack on the web-application side. We’re using bulma for the CSS. Of course as we’ve already mentioned, the TurtleCoin network interaction is powered by wallet-backend-js. I’m also using several tools to make up the development environment like eslint and prettier for code linting and formatting, and react-hot-loader for hot refresh in dev mode._

With a list of technologies like that you’re bound to snag someone’s attention! Extra, thanks for this interview. Is there something we didn’t cover that you want to share with everyone?

_Thanks for having me! I’d just like to say thanks again to the TurtleCoin community and especially the developers that have helped me along my path to becoming a dev; particularly zpalm, ibmcd, sue, rock, fexra, and anybody else that’s helped me out along the way. Because of you all I’ve discovered something new that I’m really passionate about and I see myself doing for the rest of my life. I also look forward to getting more actively involved in core development and leaving my own mark on the core TurtleCoin codebase._

> Check out ExtraHash’s handywork in the latest release of Proton GUI Wallet at [https://getproton.org](https://getproton.org/)
>
> If you’re a beginner developer or want to learn more and help out, check here for some good first issues to get started with <https://github.com/turtlecoin/turtle-wallet-proton/issues>

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/from-newbie-to-core-contributor-w-extrahash/)_._
