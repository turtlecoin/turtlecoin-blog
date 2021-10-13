---
layout: "post"
title: "Mess With The Best…"
description: "A relentless Turtle Team prepares for battle! Mess With The Best… … and Die Like The Rest. TurtleCoin Feb 12, 2018 · 2 min read A critical security issue..."
image: "{{ site.baseurl }}/images/0JtrE4wwY5SDpVgk6"
date: "2018-02-12T03:20:17.946Z"
---

![Image result for hackers phone booth](https://miro.medium.com/max/1000/0*JtrE4wwY5SDpVgk6.)

[A relentless Turtle Team prepares for battle!](https://www.ayrx.me/cryptonote-unauthenticated-json-rpc)

## _… and Die Like The Rest._

_A critical security issue was discovered by Turtlecoin developers and subsequently patched. Other Cryptonote forks and, possibly, other coins are vulnerable as well._

**If you have not already done so, please update to the** [**latest version of Turtlecoin**](https://github.com/turtlecoin/turtlecoin/releases/latest)**.**

Turtlecoin is completely secure from the vulnerability described in this article from v0.3.1 onwards. Technical details are published here: <https://www.ayrx.me/cryptonote-unauthenticated-json-rpc>

Roughly two weeks ago, some of our developers decided to look into the security of Turtlecoin. It was immediately apparent that the vulnerability Tavis Ormandy pointed out in the Electrum Wallets (<https://twitter.com/taviso/status/949804775473737728>) were also present in Turtlecoin as well as most Cryptonote forks.

**We immediately set out to fix this in two commits:**

1. <https://github.com/turtlecoin/turtlecoin/commit/4949e91e09bc1d16132090aef4dc09cc6ca09fa1>
2. <https://github.com/turtlecoin/turtlecoin/commit/7a966b40f3e967974982321c3ccc1a50265d355d>

Additionally, we have also reached out to the majority of the other affected Cryptonote coins with our findings in an effort to secure the community and to raise awareness for the bug class.

The impact of the vulnerability is substantial. A simple hosted webpage could allow an attacker to steal funds from an open wallet as a victim surfs the internet without any interaction from the victim at all. This drive-by attack would not alert the victim until it is too late and the funds are gone.

**We recommend that users of other coins exert extreme caution when using their wallets and to avoid clicking on links sent by untrusted individuals.**

> **Note:** Thanks to the members of the Turtle team that worked hard to patch and disclose this issue responsibly. We hold your safety as our first priority, and tests like this help us hold that commitment. — RockSteady
