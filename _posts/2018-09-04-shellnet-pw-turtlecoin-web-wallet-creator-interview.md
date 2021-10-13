---
layout: "post"
title: "ShellNet.pw — TurtleCoin Web Wallet Creator Interview"
description: "I took a minute to interview DSAnon, the creator of the first TurtleCoin web wallet, which he named ShellNet. This is another one of a stream of firsts considering DSAnon, because I think if memory…"
image: "{{ site.baseurl }}/images/0_V0dkDetx9PohV-O.gif"
date: "2018-09-04T00:41:12.479Z"
---

![]({{ site.baseurl }}/images/0_V0dkDetx9PohV-O.gif)

## Not bragging or anything but… TurtleCoin’s got a web wallet now.. It has blackjack, free beer and spinning rims! Check it out!

_I took a minute to interview DSAnon, the creator of the first TurtleCoin web wallet, which he named_ [_ShellNet_](https://shellnet.pw/)_. This is another one of a stream of firsts considering DSAnon, because I think if memory serves me right, he was the first person to buy TurtleCoin with outside funds, almost a year ago._

_Take a second to check out the interview, try out the web wallet, and if you want a few TRTL’s to kick the tires with,_[ _just give us a shout in the chat and we’ll get you set up with some starter funds._](http://chat.turtlecoin.lol/)

![TURTLES ARE SAFE](https://miro.medium.com/freeze/max/60/0*_661oumpwTm6fIC0.gif?q=20)

![TURTLES ARE SAFE](https://miro.medium.com/max/1360/0*_661oumpwTm6fIC0.gif)

TURTLES ARE SAFE

## **RockSteady (TRTL)**

Hey man thanks for agreeing to the interview! So tell me, how does it feel to be the first guy to have a TRTL web wallet?

**dsanon**

At first it didn’t seem like a big deal, but now that there’s about 150 users it’s a big responsibility. The responsibility on me to keep ShellNet up and running securely has kept me up at night on several occasions.

**RockSteady (TRTL)**

That’s cool! You know, a big draw to people who use your web wallet is that you can get started much faster than syncing a normal wallet (Currently, it takes at least 2 hours and 36gb to sync the regular wallet). Everyone tells me “shellnet is FAST”, which is crazy for a Turtle themed site

Can you tell us about how long it takes to sign up and make a wallet?

## **dsanon**

It takes about a minute to signup. all you need is a username and password. users can choose any password they want, secure or insecure. The authentication method (Secure Remote Password) doesn’t store the hash, the only way to break in would be though bruteforce methods. I plan on implementing 2FA soon to make accounts even more secure

![Once you make an account you should immediately backup your keys. if ShellNet goes down for maintenance you can use the same wallet on your local pc.](https://miro.medium.com/max/60/0*VZ0GyLaqVP3kT3gG.png?q=20)

![Once you make an account you should immediately backup your keys. if ShellNet goes down for maintenance you can use the same wallet on your local pc.](https://miro.medium.com/max/1400/0*VZ0GyLaqVP3kT3gG.png)

Once you make an account you should immediately backup your keys. if ShellNet goes down for maintenance you can use the same wallet on your local pc.

**RockSteady (TRTL)**

So, how long does a user have to sync after the 1 minute signup? Is there syncing at all? Does it use any space on the user’s hard drive? (sounds like weird questions, but people will want to know)

**dsanon**

The wallet is always synced to the blockchain. you can start to receive and send TRTL as soon as you signup without having to download a 36gb+ blockchain

**RockSteady**

That’s good to hear. So you mentioned backing up my keys.. If I set up a full wallet later on my computer at home, and I take these keys from my web wallet and use them on my home wallet too, without converting it or anything?

**dsanon**

Yep, it’s just that simple

![The interface is so simple, you'll pick it up right away](https://miro.medium.com/max/60/0*0XUPxSjT5BnNjL6k.png?q=20)

![The interface is so simple, you'll pick it up right away](https://miro.medium.com/max/1400/0*0XUPxSjT5BnNjL6k.png)

The interface is so simple, you’ll pick it up right away

**RockSteady (TRTL)**

That’s really cool. What’s some of the technology running behind it? I hear there’s some interesting stuff under the hood.

**dsanon**

The backend is written in Go and the front end is just simple HTML and Javascript. I’m using the microservices application architecture so I can easily scale ShellNet in the future. the coolest part is the authentication. I’m using the secure remote password protocol which is a type of zero knowledge password proof. there’s no password equivalent data stored in the database. instead, the verifier generated during signup is saved, and when you login another verifier is generated and the verifiers are compared.

If you want a better explanation of SRP and why it’s more secure than just saving a hashed password check out this video <https://youtu.be/RWksEY-Bf9I>

[SRP: Never store — or even know — your user’s passwords! (Markus…](https://youtu.be/RWksEY-Bf9I)

![]({{ site.baseurl }}/images/0r9tge0oyCDUVGsiv.jpg)

**RockSteady (TRTL)**

Nifty, What are your plans for the web wallet in the future? What’s next on your plate?

**dsanon**

The main ones are: sending messages (encrypted or unencrypted) in the blockchain and qr code based two factor authentication.

**RockSteady (TRTL)**

Hey great idea, tell me more about the messaging feature, what do you have in mind?

![]({{ site.baseurl }}/images/0yJdaoTUU6P6De_T9.png)

**dsanon**

when sending TRTL, you can also send a text message. the message will be converted to base16 and stored in the tx_extra field of the transaction. sending encryped messages will only be supported if you’re sending to another ShellNet user.

**RockSteady (TRTL)**

Can’t wait to see that feature on the site, I think that will be really popular! Great work so far! Is there any way the community can help your development or is there a tip address where they can donate back to you?

**dsanon**

Yes, my donation address is

> TRTLuySpDqd2fcvq5vx7Jiayw6yao7JHXFPuia5V83cVREtQSKyvWpxX9vamnUcG35BkQy6VfwUy5CsV9YNomioPGGyVhK3YXLq

There is also a discord if you need support <https://discord.gg/C2as5Yt>.

**RockSteady (TRTL)**

Thank you for doing this interview, I hope many Turtles check out the service! Thanks for all of your hard work

Is there anything you’d like to add?

**dsanon**

That is all. thanks for the interview Rock!

**RockSteady (TRTL)**

Any time!

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/shellnet-pw-turtlecoin-web-wallet-creator-interview/)_._
