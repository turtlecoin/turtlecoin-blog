---
layout: "post"
title: "What The Fork?!"
description: "There are a few types of forks, and the goal here is to give you a basic understanding of all of them so nobody has to be afraid of what they mean. If you have questions, or want to talk more, you…"
image: "{{ site.baseurl }}/images/0M59JocdGXRMrYG4j.jpg"
date: "2018-09-02T19:09:54.398Z"
---

![]({{ site.baseurl }}/images/0M59JocdGXRMrYG4j.jpg)

## Fork this, Fork that, Fork yer mom, Fork you too. Let’s get to the bottom of this whole forking deal and talk about what the fork is going on!

There are a few types of forks, and the goal here is to give you a basic understanding of all of them so nobody has to be afraid of what they mean. If you have questions, or want to talk more, you can [catch us in Discord.](http://chat.turtlecoin.lol/)

## Type 1, the “GitHub Fork”

We use a website to hold our code called GitHub. GitHub lets nerds from across the globe collaborate on the same project at the same time, with all of the changes recorded to see where something broke along the way.

![It really helps us when people click the star and follow us, but it super helps us when you fork the code and make a pull request](https://miro.medium.com/max/60/0*76YZWuVfR0I1S6Ig.png?q=20)

![It really helps us when people click the star and follow us, but it super helps us when you fork the code and make a pull request](https://miro.medium.com/max/952/0*76YZWuVfR0I1S6Ig.png)

It really helps us when people click the star and follow us, but it super helps us when you fork the code and make a pull request

In order to write code for TurtleCoin, you have to _fork_ the code on GitHub, which just means clicking a button that says “Fork” in the top right corner. This just puts a copy of the code in your workspace so you can work on your part of the project without interfering with others, and then when you are done, you create a “pull request” which asks the main TurtleCoin project to pull in your changes. That’s why it’s called a _pull request_.

![These are all of the TRTL Forks](https://miro.medium.com/max/48/0*0LMSYlJN74xxpCQr.png?q=20)

![These are all of the TRTL Forks](https://miro.medium.com/max/1400/0*0LMSYlJN74xxpCQr.png)

These are all of the TRTL Forks

This can also be someone creating their own _fork of TurtleCoin_ which is something we support, and have written guides how to do. Forking our code is not stealing anything, and it even helps us rank higher on CoinGecko, which measures the amount of developer attention a certain project receives. Our license specifically allows for other projects to use the TurtleCoin code as a base for their projects and learning, as long as they give others the same chance. This helps the community learn about how the project works, and helps us spot bugs and errors before they become bigger problems by having more eyes on the prize.

## Type 2, the “Soft Fork”

This is the second most common type of fork. We commonly refer to this as a fork upgrade. When you’ve been gone a while, and you come back and notice your old software wont go past a certain block on the network anymore, you’ve likely missed a soft fork upgrade. A quick update of the daemon will get you back on the network and your funds are right where you left them.

So what’s a soft upgrade _do_ anyway? Well, it’s hard to come up with a real life comparison, but to put it in simple terms, the entire network has to agree on how blocks are produced, and when we create an upgrade to the format of how blocks are made or validated, then we have to place a bookmark in the chain that says “ok, people should be upgraded by the next 3 weeks, so anything after that needs to be running the next version to keep going”.

This does not create two chains, and this does not create free money. The old chain branches off and stops, the main chain keeps moving.

Future updates to the software will enable us to drop old clients from the network that haven’t updated, and give them a gentle message urging them to upgrade their software to regain access.

![IS YOUR FORK HARD OR NOT](https://miro.medium.com/max/60/0*2hkMpe4iyWdxA_lG.jpg?q=20)

![IS YOUR FORK HARD OR NOT](https://miro.medium.com/max/1120/0*2hkMpe4iyWdxA_lG.jpg)

IS YOUR FORK HARD OR NOT

## Type 3, the “Hard Fork”

This type of fork is least common, and like in the Bitcoin and Ethereum world, is a result of a section of the network deciding to change the rules and the network_id and new seed nodes to create their own network signature and branch off from the main chain.

This type of hard fork is called a hard fork because the software has to be hard-coded to accept the new changes, which would consist of adding new seed nodes, removing old ones, and assigning a new network ID and so on.

![THIS KID KNOWS THEIR SHIT](https://miro.medium.com/freeze/max/60/0*N-JYWgFU6rUO_Ky0.gif?q=20)

![THIS KID KNOWS THEIR SHIT](https://miro.medium.com/max/1400/0*N-JYWgFU6rUO_Ky0.gif)

THIS KID KNOWS THEIR SHIT

This creates two chains that continue independently of each other, but does not necessarily give you double the coins, as the demand for the secondary currency doesn’t magically appear overnight.

## 4th Place, Honorable Mention, the “Network Fork”

These happen all the time, and they are always resolved automatically by the network, behind the scenes. When you see anything about “Resolved” on your daemon, that means a network fork was detected and resolved.

What this means is that two miners reached the conclusion to the same block at roughly the same time and momentarily, the network allowed both chains to continue while the rest of the network decides which one grows longer over the next few blocks. This is nothing to worry about and is what an orphan blocks is.

This is almost always because people are adding hash power to the network in bursts when the difficulty is low. It causes the network to spit out blocks quicker than normal, and raises the chances of two pools hitting the same result at the same time.

![Image result for haha stupid fucking bcash forkers you fucking rubes i cant believe you thought that would work meme latest](https://miro.medium.com/max/60/0*YrXbgdhCw70ViW1m.jpeg?q=20)

![Image result for haha stupid fucking bcash forkers you fucking rubes i cant believe you thought that would work meme latest](https://miro.medium.com/max/1400/0*YrXbgdhCw70ViW1m.jpeg)

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/what-the-fork/)_._
