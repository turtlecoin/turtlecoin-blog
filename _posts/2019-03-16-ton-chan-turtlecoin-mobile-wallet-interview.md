---
layout: "post"
title: "Ton Chan TurtleCoin Mobile Wallet Interview"
description: "One of the things that has been most requested of us is a mobile wallet. In the past we’ve always pointed mobile users to our web wallets, but a brave turtle came forward and put together a cool…"
image: "{{ site.baseurl }}/images/0-7NLKCW7q3hHadoJ.gif"
date: "2019-03-16T06:11:50.885Z"
---

![]({{ site.baseurl }}/images/0-7NLKCW7q3hHadoJ.gif)

_One of the things that has been most requested of us is a mobile wallet. In the past we’ve always pointed mobile users to our web wallets, but a brave turtle came forward and put together a cool android wallet and we’re pretty stoked about that, so here’s an interview with the creator!_

![Image result for ton chan](https://miro.medium.com/max/1000/0*4bbGJEovwgtUOAG_)

A wild Ton Chan appears!

RockSteady: Zpalm, thanks for taking the time to do this interview. You’re the first person to come up with a mobile wallet- with us being a year in, why do you suppose nobody else came up with anything in this time? There must have been significant roadblocks.

Zpalm: There are a couple of things that make a mobile wallet tricky. The first one is that you need quite a lot of cryptography code. ed25519 libraries are pretty common, however, they normally don’t expose the primatives we need. Implementing this is not too tricky, but it’s quite a bit of work. I ported the C code to C# for turtlecoin-cs, and it was quite a pain to do. I didn’t need to do this for the mobile wallet, since I’m using the turtlecoin-utils library. This library takes the core C++ code, and compiles it to JavaScript. Since the mobile-wallet is written in typescript/javascript, that was a big chunk of code I didn’t have to write. You also need the core cryptographic functions for the wallet to operate, like creating key images, generating ring signatures, and so on. Secondly, actually managing a wallets operation is a little tricky. The sync process is relatively simple, once you understand how to piece together the different cryptographic operations, but there are quite a few pitfalls which can make you miss blocks when syncing, or miss transactions. I had already learnt a lot on how to design a wallet backend when I rewrote the C++ wallet backend, so porting that over to typescript wasn’t too much of a chore. The majority of the code of the mobile wallet is in that external backend library — the frontend is pretty easy to do, just a bit slow to get everything looking nice.

RockSteady: TonChan is an interesting name, where did that come from?

Zpalm: There’s a nice quote, ‘There are only two hard things in Computer Science: cache invalidation and naming things.’ Finding a cool name which is somehow based on turtles was a bit tricky, so I nabbed the name of a cute Turtle, called Ton or Ton-chan from an anime, K-ON!

![]({{ site.baseurl }}/images/0SqMFEuvfDJlrofGz)

RockSteady: What features have you seen others talk about? Anything you think is interesting enough to implement?

Zpalm: One of the things I really like and I think some other people have commented on is how easy the transfer process is. If the payee is already in your address book, it’s one tap along with entering the amount to send a transaction. I plan on making this even faster — I’m currently working on implementing support for QR codes which have an amount+name attached — this will allow you to scan one QR code, and it will add the user to your address book, and pop you right on the confirmation screen. This feature is also supported by TurtlePay, so I think that can help with adoption — It’s easy to use TurtleCoin to accept payments, and it’s easy for users to pay with as well. Other features that have been requested is address book management, fusion transactions, dark mode, and more. Most of them I had already planned to add (and haven’t got round to yet). The dark mode one was interesting — I thought it would be pretty trivial to implement, but it ended up being a bit of a pain getting the theme to apply everywhere when changed. This led to a redesign of the theming process, and now it’s would be pretty easy to add support for user created themes. I’m not sure how many people would make use of a feature like that, maybe we’ll see it added.

RockSteady: Great answer, can you tell us a bit about what the wallet can do currently, and what you have on the development roadmap?

Zpalm: The wallet is perfectly functional as a daily use wallet. It can send transactions, receive transactions, and view past transactions. Not that much more a wallet needs! However, there are a number of other features to make the experience nice to use. One feature I’ve really been liking, and I think other people have been too is the notifications. It’s a very simple feature, but it’s quite nice to get a notification whenever you get sent a transaction. The roadmap right now is adding a few more features like fusion transactions and fixing up a few bugs have been experiencing, then iOS support.

RockSteady: Id also like to talk a bit about development, whats the app written in? What was that process like, if you had to explain it to a non developer?

Zpalm: There’s a few components of the app. There’s the frontend, that’s the UI, and so on, that the users see. That’s written in JavaScript, using React Native — A framework to write apps for both iOS and Android using JavaScript. Then there’s the backend, which manages the syncing process, sending transactions, managing balance, and so on. That’s written in Typescript, which if you’re not aware, is basically JavaScript, with optional typechecking. Helps you avoid some easily fixable bugs, like using variables that aren’t defined. Finally, there’s a high performance section written in C++. The wallet syncing process is quite CPU intensive, and sadly, the JavaScript cryptography code is slow as molasses — It can process something like 1 block a second. This was one of the big roadblocks when implementing the wallet. What I ended up doing, is we take the block data in JavaScript/Typescript land, then pass it through to the Java ‘bridge’. Most android apps are written in Java, and this is where the real work in React Native goes on. From there, we can pass to the JNI (Java Native Interface), which lets us call C or C++ code. We process the block in C++, then pass the results back to Java, then finally back to JavaScript/Typescript. This adds a little bit of overhead, but ends up being a lot faster than processing in JavaScript — It’s something like 15–50 blocks a second, depending on your phones power. Still quite slow compared to desktop wallets, but hey, that’s one of the downsides of using a mobile.

RockSteady: What was that process like, if you had to explain it to a non developer?

Zpalm: Writing the UI was pretty frustrating — Trying to get everything to line up nicely, and all coloured in a nice looking way. Since you’re lining things up by pixels, or percentages, instead of dragging and dropping, there’s a lot of changing a value, reloading, and seeing how it looks. I found sometimes I’d have spent 3 hours and only written 50 lines of code for a screen I was designing. I’m very pleased with the final outcome, but it is sloooow to get there. Writing the backend was business as usual, since it’s not locked to just mobiles, I could test this all out on a desktop, rather than an android emulator, which makes developing a lot faster. Since I had done most of this work in the C++ already, it was pretty trivial, just copying code over and converting into the typescript equivalent Writing the high performance code was painful. Since you were working in three different languages, it was a pain to figure out where in the process you had gone wrong. If you ever did anything wrong, you pretty much always got an app crash, rather than a helpful error. The documentation on how to use the API is pretty sparse, so there’s a lot of googling to figure out how to do something pretty simple. After a lot of scraping logs, finally got it doing the right thing. I was stumped for a few hours by accidentaly swapping two parameters around

RockSteady: Given the popularity of the android app, do you think there’s interest in an iOS app, and what hurdles do you think someone might face in implementing it on iOS? Is there anything they could learn from your journey with the Android app?

Zpalm: Certainly, one of the most requested things is an iOS app. Since the wallet uses React Native, which is cross platform, there’s not that much that needs doing for iOS support. The main thing we need is to implement the high performance C++ code in iOS as well — since the Java/JNI stuff is android only. Since iOS uses objective C, which is a superset of C (All C code is valid Objective C code), this shouldn’t be too tricky — but I might have to change from C++ to C, which could be a pain. We’ll also need to make sure that everything looks good, and fits with the iOS theme — they have a few differences, and we want to try and make the wallet feel like a native iOS app, if possible. There’s a few things which I’m not sure what the iOS pattern is — like ‘Toast’ notifications on Android (Those little messages which pop up in a bubble at the bottom of your screen) that we’ll need to add.

RockSteady: How many people have downloaded TonChan so far? Have there been any interesting bugs reported? What is the best way someone can contribute to the project?

Zpalm: Google play is telling me 104, it takes a little time to update but that’s already a decent amount for something released only a week or two ago. The most interesting bug is probably the wallet sync slowing down when you swapped tabs — I think I fixed that one, but it was quite puzzling at first. The best way to contribute is to leave an issue on the github if you see something not working, or something that you think could be improved, which as much info as possible. Of course, if you’re a developer yourself, you could try and fix it too!

RockSteady: Tell me a bit about TonChan’s relationship w/ TurtlePay, I heard there’s something in the pipeline regarding fees

Zpalm: TurtlePay and TonChan work very well together in my opinion, TurtlePay making it easy to request payments, and TonChan making it easy to send payments. We’re going to waive any fees (other than the mandatory network fee) for TurtlePay transactions to help guide adoption.

RockSteady: That’s a pretty solid description, what advice do you want to give the person who ports it to iOS?

Zpalm: I hope iOS gives better errors when native code breaks than Android! I forgot to mention this earlier, but background syncing is another big hurdle for the wallet. When using React Native, there’s no way to just run our app forever, and sync in the background, unfortunately. Both Android and iOS allow us to fire an ‘event’ every 15 minutes, which we use to wake up the wallet and sync it. On Android, this event seems to be able to last as long as we like, so we run the sync for 14 minutes, then go back to sleep to wait for the next event. On iOS however, this event can only run for 30 seconds, which is obviously not very long. I don’t know if there’s any way around this, I couldn’t find any when I was searching. iOS also schedules the events with a proprietry algorithm — so they may end up never running, or just running once a day. This is going to probably be the biggest pain point to get around when porting to iOS.

RockSteady: As with most TRTL projects, we want to reach out to the community to help with things and give folks a chance to put their mark on the app, what are some “good first issues” for someone wanting to get started contributing to TonChan? Are there any features you’d like to see that you’re looking for collaborators on? What toolchain stuffs and helpful bits would someone need to follow in your foot steps and tinker around?

Zpalm: There are a couple of ‘Good first issues’ listed on the Github — <https://github.com/turtlecoin/turtlecoin-mobile-wallet/issues> — but frankly most of the things there aren’t too tricky to add. One not listed there but that would be very helpful is improving the setup guide. It’s kinda confusing to get the android studio setup done correctly, and an emulator running, which as you mention, would be needed to test things. I don’t think there are any huge features which we’d need collaboration on yet, aside from iOS support. If you’re wanting to implement something and are having issues, give me a ping and I’ll be happy to help you through them

RockSteady: What has it been like developing with React Native? For any developers out there considering it over something more conventional , what advice or forewarning would you give? How does it contrast from web apps written in React?

Zpalm: It certainly makes writing the UI nice. The react model of state always traveling down can be a little tricky to get used to, but once you’ve got the hang of it then it can be pretty fast to develop in. You can also use the majority of nodejs modules, however, you are likely to need a project like <https://github.com/tradle/rn-nodeify/> to get them to work correctly, the setup is a little hacky. You will find some modules work perfectly in node, but a certain feature doesn’t work in react-native, which can be a little frustrating.

I would also advice against the react-navigation library — TonChan is using this to navigate between different screen, and it works OK, but some simple things, like going back to a specific screen are done in a very confusing way. I’ve heard good things about the wix library to replace this. If you need fine control over the Android OS, like running background/foreground services, then react-native is probably not for you. While you can write Java code and call it from react-native, it’s quite cumbersome and hard to integrate with the rest of your app. I would have liked to be able to launch a foreground service, but there’s currently no react-native modules which allow this, short of doing it yourself. Then, all your application code that runs in that service would have to be in Java, not JavaScript. Finally, all react-native code runs on a single thread, as that’s how JavaScript works. If you have high performance code, this may block the UI from rendering. So, pros include cross platform support, fast development, lots of libraries available, cons include somewhat hacky setup, single threaded execution, and not as fine grained integration with the OS.

RockSteady: Would you ever consider pure Java or Kotlin in the future?

Zpalm: Kotlin, maybe. I’ve written very little Java, but the small experience I had with it was poor, simple things were very verbose, and it looked no fun at all to develop in.

RockSteady: What was the process like boarding a crypto wallet app in the Google Play store? I know it’s been a bit of an uphill battle for people to get their wallet apps in the iOS app store. Can you walk us through the process of how you went from “now I have an app” to “now i have an app on the app store” and what all it entails being an “android developer”Also, please detail the costs and wait times involved.

Zpalm: It was really easy, to be honest. I just had to sign up for an account, send them $25, add some images to display in the store, and upload the apk. I think it was less than 24 hours from uploading my apk to it being live on the store.

Zpalm, thanks for the internet and thanks even more for the mobile wallet. It’s great seeing it grow as a project and I can’t wait to see who puts together the next great PR for it :D

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/ton-chan-turtlecoin-mobile-wallet-interview/)_._
