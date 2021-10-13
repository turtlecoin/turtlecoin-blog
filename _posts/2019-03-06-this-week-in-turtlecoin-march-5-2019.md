---
layout: "post"
title: "This Week in TurtleCoin (March 5, 2019)"
description: "TonChan Mobile Wallet — Hello, As you may be aware, a mobile wallet for Android was recently released on the play store. We’re planning on doing a full article on that, so I’ll just keep it brief on…"
image: "{{ site.baseurl }}/images/0Ys48xv9zL4jDGcWi.png"
date: "2019-03-06T06:01:33.420Z"
---

![]({{ site.baseurl }}/images/0Ys48xv9zL4jDGcWi.png)

## Developer Updates

![]({{ site.baseurl }}/images/0l2Cexm8WeXijPziq.png)

TonChan

**TonChan Mobile Wallet —** Hello, As you may be aware, a mobile wallet for Android was recently released on the play store. We’re planning on doing a full article on that, so I’ll just keep it brief on the latest changes, with v0.0.4\. I added a dark mode, along with a more comprehensive theme system. There’s a slight bug with v0.0.4 on the settings page on some resolutions, but this will be fixed in v0.0.5\. I added support for Android 4, for those of you who are still running potatoes. I’m not sure if the support goes any lower than that. I also added a logger screen, to help fix any weird hard to pin down issues. Finally, I fixed the USD/currency value only updating on app launch. Along with a few other bug fixes. In v0.0.5, I’m planning on adding support for address+amount QR codes, so you just need to scan one qr code and hit confirm to send a transaction. If there’s something you’d like to see, or something that’s not working, please make an issue on the Github linked. Or if you’re a developer, maybe you can help add some of the already requested features? :) **— Zpalm**

[turtlecoin/turtlecoin-mobile-walletA mobile wallet where you own the keys, using TypeScript, JavaScript, and React Native …github.com](https://github.com/turtlecoin/turtlecoin-mobile-wallet)

**TurtleCoin Multisigs** — I believe I have the lion’s share of the multisig cryptography done; however, I’ve encountered an issue in generating composite key images so that transactions can then be generated from those. I’ll then need to make sure that the signing input signing works correctly before attempting to add multisig support to any wallets. **— IBurnMyCD**

![]({{ site.baseurl }}/images/0tOkI5jccZRq_EqJh)

“TurtleCoin is up to 39 forks! Plus maybe 5 I need to get around to adding.” — Turtley McTurtleton McDrizzle @ ForkMaps.com

**TurtleCoin Block Explorer** — I spent a bit of time last week adding a few new features to the official block explorer. It now contains a client-side wallet generator, address decoder/encoder, and a random payment ID generator. I’ve also added additional network charts that depict some of the network statistics for the last 24 hours. For those of you that have asked about TurtleCoin emission rates and a graph to help better understand that emission, I’ve also added a Currency Supply & Emission graph using the base reward as specified in core code. **— IBurnMyCD**

[TurtleCoin Block ExplorerBlock Explorer for the TurtleCoin network that is a fun, fast, and easy way to send money to friends and businesses.explorer.turtlecoin.lol](https://explorer.turtlecoin.lol/)

![]({{ site.baseurl }}/images/0A9a5SNlLlN4jblNM.jpg)

**CuvéeARM Turtlepool —** As if we at Cuvée labs would have nothing to do already, we were curious if we could run a pool on the ARM platform (better known as Pi boards). The set up is still crazy and nowhere near production ready (we followed the quick and dirty approach of putting everything — the daemon, the HA scripts with PMě, Redis, the pool and the webserver all on one OrangePI). Fired all up and voila, the pool works. Now, let us add some miners, so we redirected all our OrangePI One Plus miners, as well as the GPUs to our new pool. We run it experimentally as a private pool only for now, current hash-rate about 40KH/s, did not found a block yet, so … if this whole thing does not crash & burn, expect more news next week. Our goal? Run a public pool on these ARM-boards, properly distributed and ready for scaling up and out! **— LeoCuvée#1481**

**Tscripta** — Hello there, i will be working on reviving my old project that is probably outdated by now. It will try to emulate loafwallet (i like its style) and add additional features that t-scripta lacked **— Val#1969**

![This guy knows his Turtles](https://miro.medium.com/max/60/0*UWEUNYF4FeK6Ukur.png?q=20)

![This guy knows his Turtles](https://miro.medium.com/max/1400/0*UWEUNYF4FeK6Ukur.png)

“low quality memes > soulless high quality memes” — the always-insightful Zpalm, 2019, #general

## Good First Issues

_Lately we’ve been hearing from a lot of you “how can I become a developer on the TRTL Team?” so Zpalm assembled a bunch of easy-wins for someone just getting started to get their feet wet with our code. These have been marked with “Good First Issue” on GitHub for visibility, and we’ll be highlighting them in the roundups in the coming weeks for more visibility._

- [**add RPC method to validate address** https://github.com/turtlecoin/turtlecoin/issues/733](https://github.com/turtlecoin/turtlecoin/issues/733)
- [**Add https support to cpp-httplib/nigel** https://github.com/turtlecoin/turtlecoin/issues/713](https://github.com/turtlecoin/turtlecoin/issues/713)
- [**Support Blockchain cache API in Nigel** https://github.com/turtlecoin/turtlecoin/issues/712](http://support/%20Blockchain%20cache%20API%20in%20Nigel)
- [**Add a logger to WalletBackend** https://github.com/turtlecoin/turtlecoin/issues/709](https://github.com/turtlecoin/turtlecoin/issues/709)
- [**Prune spent inputs after some period of time from WalletBackend** https://github.com/turtlecoin/turtlecoin/issues/708](https://github.com/turtlecoin/turtlecoin/issues/708)
- [**Daemon+WalletBackend timestamp adjustments** https://github.com/turtlecoin/turtlecoin/issues/704](https://github.com/turtlecoin/turtlecoin/issues/704)
- [**Display unlock time / timestamp in** list/incoming/outgoing_transfers zedwallet/zedwallet++ https://github.com/turtlecoin/turtlecoin/issues/675](https://github.com/turtlecoin/turtlecoin/issues/675)

## Free TRTL Advertising

- Mining4Vets Cn-lite-v7 13kh Rig specs: 4x MSI Gaming X RX570 4GB 1x XFX RX 580 8GB 1x MSI Armor RX580 4GB 1x MSI Armor RX570 4GB BONUS AEON CLASSIC — not required to be mined for bonus 24hrs = 50 xmlc 48hrs = 110 xmlc 72hrs = 180 xmlc 96hrs = 260 xmlc 120hrs = 350 xmlc 144hrs = 450 xmlc 168hrs = 560 xmlc
- Mining4Vets CN-Lite-V7 BONUS 24hrs = 50 xmlc 48hrs = 110 xmlc 72hrs = 180 xmlc 96hrs = 260 xmlc 120hrs = 350 xmlc 144hrs = 450 xmlc 168hrs = 560 xmlc <http://rig.rent/rigs/120718>

## Fork Watch!

![]({{ site.baseurl }}/images/03VyvyhRhmM8_fEfN.png)

**Kegcoin Gold —** Cheap transactions and super fast, 100 % private transactions for everyday use — <https://github.com/kegcoin-project/kegcoin-gold>

## Shoutouts & Thanks

Thanks to Fipsi for donating his skills toward our project. Same goes to the rest of you. — Mining4vets

Thanks devs keeping mining CPU&GPU mining fair not ASIC — Liu

Zpalmtree has done fantastic work for the mobile wallet! If you arent using it yet you should be. — afterconnery

Just a big thank you to all the active turtles — Bernd

I recently bought a couple of TurtleCoin t-shirts from mosu-forge’s store. They accept TurtleCoin! Check it out — [https://trtl-store.com/ — Zpalm](https://trtl-store.com/)

Thanks to CapEtn for his PR’s and testing of the mobile wallet :) — Zpalm

Shouts out to all the community members I see being classy and representing Good Turtles in other Discords. I’m always proud when I go exploring and see everyone keeping on their best even when they’re away from home. The positive influences are infectious. — RockSteady

Shouts to Loki devs and other recent projects for choosing CN_Turtle — the miner community loves the new algo from what we can tell, and we’re glad you guys are giving it a spin! — RockSteady

_Originally published at_ [_TurtleCoin_](http://blog.turtlecoin.lol/archives/this-week-in-turtlecoin-march-5-2019/)_._
