---
layout: "post"
title: "How A Block Is Born"
description: "This is a chat snippet between TurtleCoin Developer Bebop and Atakor, from a time when Atakor asked about how blocks are formed. Bebop gave…"
image: "{{ site.baseurl }}/images/0gOz6_ISxqBqmy6Ho.jpg"
date: "2018-02-03T01:15:48.574Z"
---

_This is a chat snippet between TurtleCoin Developer Bebop and Atakor, from a time when Atakor asked about how blocks are formed. Bebop gave a great description, and recently Hai brought it to my attention that it never got posted. I felt it was best to leave it raw and unedited, so excuse any LOL’s or spelling mistakes please. Thanks Hai for bringing this to my attention._

![]({{ site.baseurl }}/images/0gOz6_ISxqBqmy6Ho.jpg)

image credit: Malware Bytes

# Atakor-01/16/2018

this is not really offtopic but i don’t want to pollute general and interupt the ongoing discussion: how are transactions validated in cryptocurrencies, specifically PoW ones?

# Bebop van Saberhagen-01/16/2018

well in a nutshell laymen’s terms each block is a hash of the previous block and some digital signature information from the sender and the solution to the PoW and the miner

it uses cryptographic key pairs so that it’s basicalyl pretty easy to verify the validity using the public keys — where it’s computationally difficult to try to reverse the private keys used to sign all the information

# Atakor-01/16/2018

so noone has to do anything “manually” to verify transactions

everything is automated

# Bebop van Saberhagen-01/16/2018

correct

# Atakor-01/16/2018

mining = generating coins + validating transactions

# Bebop van Saberhagen-01/16/2018

yeah so it’s like this

# Atakor-01/16/2018

k great, thanks, i’ll check all the technical details on how it’s done later

# Bebop van Saberhagen-01/16/2018

the blockchain is just a ledger right

# Atakor-01/16/2018

i’m curious but never took the time to really understand the whole thing

yep it is

# Bebop van Saberhagen-01/16/2018

well first let me ask you this

do you know what a hash is?

# Atakor-01/16/2018

yes

# Atakor-01/16/2018

was going to say, i’m a computer science graduate just didnt take time to read the details on how the whole thing works

i understand everything on a superficial level

# Bebop van Saberhagen-01/16/2018

ok awesome

just don’t want to explain stuff you already know

# Atakor-01/16/2018

yeah ofc

# Bebop van Saberhagen-01/16/2018

ok so think of it like this

let’s say we’re a group of friends and we create a currency. we agree there are 100 units of fartcoin there’s 10 of us in the group and we all put it in 10 bucks in a pot and say our 100 units of fartcoin are worth the 100 dollars in the pot…

now we decide instead of printing out or making physical tokens for this currency we’re Bebop van Saberhagen-01/16/2018

ok so we say any time anyone transacts, the transaction isn’t official unless the spreadsheet is updated.

so we agree that [@Atakor](http://twitter.com/Atakor) is going to keep up with the spreadsheet and so any time anyone does a transaction they get you to update the record. now you’re the central authority

this is bad because you could lie, for your own benefit or just because. you could get overwhelmed and fall behind or become unreliable

you could try to game the system in less apparent ways like delaying transactions in a way that gives you some advantage

# Atakor-01/16/2018

Satoshi Nakamoto, ladies & gents  
this is valuable text for beginners, i wonder if you can put it somewhere not to be lost

just goign to do it virtually

but we need a way to track the transactionso f this virtual currency right

so that you don’t sell your 10 worth to me and then tell someone else you still have it and sell it to them (double spend)

and so that once i buy 5 from you and 5 from john, now i i have 20

right

# Atakor-01/16/2018

oh

i think i know all of this actually

# Bebop van Saberhagen-01/16/2018

so we say ok we’ll make a spreadsheet

# Atakor-01/16/2018

don’t want you to go too deep

to basic i mean

i know how the tech works more or less

# Bebop van Saberhagen-01/16/2018

don’t worry i’m gonna round it out to pOw niceley here in a sec

PoW

lol

# Atakor-01/16/2018

just was confused about the validating transactions part

# Bebop van Saberhagen-01/16/2018

other people might be reading this

# Atakor-01/16/2018

ok cool

oh yeah that’s true!

# Bebop van Saberhagen-01/16/2018

ok so we say any time anyone transacts, the transaction isn’t official unless the spreadsheet is updated.

so we agree that @Atakor is going to keep up with the spreadsheet and so any time anyone does a transaction they get you to update the record. now you’re the central authority

this is bad because you could lie, for your own benefit or just because. you could get overwhelmed and fall behind or become unreliable

you could try to game the system in less apparent ways like delaying transactions in a way that gives you some advantage

# Atakor-01/16/2018

Satoshi Nakamoto, ladies & gents

this is valuable text for beginners, i wonder if you can put it somewhere not to be lost

# Bebop van Saberhagen-01/16/2018

so we say ok that won’t work we want a distributed situation. so we set up a group email and say now, for a transaction to be official, you send a message to the whole group and then everyone updates their own copy of the spreadsheet

# Atakor-01/16/2018

and to be easily accessible(edited)

# Bebop van Saberhagen-01/16/2018

but now we have a few new issues

sycnrhonization

what if everyone doesn’t see the message and update at the same time. what if soem people never get some messages, etc

and how do we know the update messages we’re receiving are legitimate

so there’s two elements to this

the first is hashing and encryption. every transaction record is just data so we can hash that, and we can hash that with the previous records. so the sender of the transaction basically does a signed hash of that and that basically gives a sequence of hashes that can be computationally verified and have mathematical guarantees of correctness and crytographic validity

now the 2nd part is consensus. how do we get everyone synced and agreeing on the same sequence of hashes

so the way we get consensus with PoW is we say ok. we’ll do updates on a sort of time interval

and for every single round, 1 random person gets to be the one to update the transactions, and that person signs it with his/her signature and then everyone gets that one as their copy

so how do we choose a random person? we don’t. we do a number guessing game, but it’s not just a simple number guessing game, it’s a hashing game

you gotta guess a number and then carry out computations on it to see if it produces the target number

and whoever guesses it first tells everyone ‘hey i got it!’ and then he can provide the solution — that is computationally easy to verify but computationally difficult to guess

think of it like a set of keys and a lock

100 billion keys or something

and you gotta go through one by one and find the right key for the lock

but once you do, it’s easy for people to insert it into the lock and verify that it opens

sorta like that, via hashing

so you if you guess that round, you tell everyone, and basically if majority quickly verifies and agrees with you, 51% or more, that’s the blockchain now

but what if no one guesses in a round?

well instead of an actual fixed time, we say a round is whenever someone finds the solution

and then we say instead of having to guess the exact number, we say you have to be within a range. and the higher the difficulty, the narrower that range, and we adjust the difficulty each round tryign to target a certain timeframe

in turtlecoin that timeframe is 30 seconds

so each round is not exactly 30 seconds but if there is more hash power then they’re gonna solve it faster and the algorithm is going to increase difficutly on subsequent rounds

and because each round takes time + computational work (hardware + electrical costs) we give a payout — a portion of our virtual currency — for solving the round to incentivize this number guessing and verifying (which we call mining) and because it is incentivized, multiple people participate and invest resources making it hard for a single entity to maintain majority by itself

now instead of a few people starting by putting money in a pot, we just say the _only_ way a unit of this currency can be put into circulation is by mining it

the ledger starts at 0 for everyone

how was that? how’d i do?

# Atakor-01/16/2018

your explanation skills are top notch

i wouldn’t have been able to formulate it as clearly and in such a continuous way

# Bebop van Saberhagen-01/16/2018

thanks

once everything is a sequence of numbers now you see how the verification is automated

so in theory i cuold tap you on the shoulder and say hey, fuck @RockSteady Nakamoto , we’re gonna make up some false transactions and send all his coins to us, even tho we don’t know the valid keys for that we’re just gonna accept it as truth(edited)

there we go

and you say yeah, definitely let’s do it

and we just agree on the fake transaction

well problem is, we’re not gonna be able to get 51% of the people to agree probably with an invalid transaction

and becuase each block is a hash of the previous

# Atakor-01/16/2018

51% is 51% of the hashing power right?

# Bebop van Saberhagen-01/16/2018

_every_ subsequent transaction would be invalid

yeah you can put it in those terms too as hashing power

now there have been cases when that has happened (ethereum)

but not everyone agreed. they forked

# Atakor-01/16/2018

or mining power should i say (de-hashing, finding the hash)

# Bebop van Saberhagen-01/16/2018

those kinds of forks can easily happen. sometimes the fork doesn’t maintain interest/value and dies or staggers along and sometimes it does well. blockchains can fork for a number of reasons

that’s where you get bitcion and bitcoin cash and what not

blockchain forks may or may not come with some software or protocol changes, but one can also deploy new blockchains with the same software and protocols or with different software and protocols

# Atakor-01/16/2018

(check PM pls)

as i told you, this explanation is valuable, you might want to save it somewhere

# hai-01/16/2018

@Bebop van Saberhagen as a non-cs graduate I found that very informative this should be on turtlecoin.lol or the welcome channel as a pinned message
