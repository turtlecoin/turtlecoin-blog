---
layout: "post"
title: "Announcing Wrapped TurtleCoin (wTRTL) on the Fantom Opera Chain"
description: "If you know someone who has problems with reading comprehension, please hold their hand gently and read them this article. I’m typing this article to prove in the most vocal way possible that there…"
image: "{{ site.baseurl }}/images/0tDUmt2Y4d26-vXDP.gif"
date: "2021-11-28T18:50:00.506Z"
---

![]({{ site.baseurl }}/images/0tDUmt2Y4d26-vXDP.gif)

Today, we're proud to announce the next step in our TurtleCoin journey. The launch of Wrapped TurtleCoin (wTRTL) on the Fantom Opera Chain. 

# What is Wrapped TurtleCoin (wTRTL)?

wTRTL is the Official ERC20 for the wrapped form of TRTL on the [Fantom Opera chain](https://fantom.foundation/what-is-fantom-opera/).

As TRTL is wrapped into wTRTL, the original TRTL is **burned** when you send it to the service address which consists of a known view key (we have public & private key) and an unknown spend key (the public spend key was [randomly generated](https://github.com/turtlecoin/turtlecoin-crypto/blob/c51c41aa9c4e3347cbc0e30ec3f1dc4712adb14d/src/crypto_common.cpp#L462)). This makes the original TRTL funds completely unrecoverable (aka. burned). The service tracks funds via payment ID contained within the integrated TRTL address the service supplies you.

**This is a one-way process.**

# Why Wrap TurtleCoin?

TurtleCoin v2 development is taking longer than expected due to real life time constraints, growing concerns of recent [quantum computing news](https://www.science.org/content/article/ibm-promises-1000-qubit-quantum-computer-milestone-2023), and other ongoing changes in the cryptocurrency industry. While everyone waits for the dust to settle on these key issues to figure out the best long term path for the project, we did not want to leave the community hanging. With all of the enhancements that everyone has been telling us about throughout the cryptocurrency industry, we figured that offering a Wrapped form of TurtleCoin could give us the runway needed to define the next evolution of the project.

# How do I wrap/swap my TRTL for wTRTL?

Visit the official swap/wrap page in the explorer that has live tracking information at [https://explorer.turtlecoin.lol/swap.html](https://explorer.turtlecoin.lol/swap.html).

Alternatively, you can access a swap interface (everything must run through the same official swap/wrap API) at:

* [https://swap.turtlecoin.com](https://swap.turtlecoin.com)
* [https://trtl.exchange](https://trtl.exchange) *coming soon per Fexra*

# Smart Contract Details

* Contract Address: `0x6a31Aca4d2f7398F04d9B6ffae2D898d9A8e7938`
* Ownership: Contract is owned by a multisig [Gnosis Safe](https://gnosis-safe.io/)
This means that a majority of the safe participants must approve the release of additional wTRTL to the wrap service or, if necessary, the minting of new wTRTL (very unlikely).
* Total Supply: 1,384,408.5531187 wTRTL
We minted the total v1 supply at the v2 swap ratio previously published (100,000:1) to avoid continuous minting throughout the wrap/swap period.
The same multisig Gnosis Safe mentioned above "owns" the total unclaimed supply and approves the wrap service to send it out on behalf of the safe.
* Decimals: 18 (yes, we gave in on this one)
* Audited: Like many ERC20 tokens, the wTRTL contract uses [OpenZeppelin Contracts](https://openzeppelin.com/contracts/) as the base contracts.
* Verification & Contract Code: Verified via [FTMScan](https://ftmscan.com/address/0x6a31Aca4d2f7398F04d9B6ffae2D898d9A8e7938#code)
* [Token Tracker](https://ftmscan.com/token/0x6a31Aca4d2f7398F04d9B6ffae2D898d9A8e7938)

# Do I need a new wallet?

Yes, you will need a wallet that works with the Fantom Opera Chain. Since Fantom is based on a lot of the same technologies as Ethereum (ETH), most of the Ethereum wallets support Fantom. Below you can find a few such wallets (not endorsements) below.

Please remember to utilize best practices for securing your wallet.

* [fWallet](https://pwawallet.fantom.network/)
* [MetaMask](https://metamask.io/)
* [WalletConnect](https://walletconnect.com/)
* [Trezor (via MetaMask)](https://trezor.io/)
* [Ledger](https://www.ledger.com/)
* [Coinbase Wallet](https://wallet.coinbase.com/)
* [Trust Wallet](https://trustwallet.com/)

# What's the minimum amount of TRTL I need to wrap?
The minimum amount to swap is dynamic as gas fees on the Fantom Opera chain vary based upon factors outside our control. As such, the gas fees provided on this page are an estimate of the fees required to transfer wTRTL tokens for each wrap transaction including transferring 0.1 FTM to the destination FTM wallet. Final gas fees are determined after the transaction on the TRTL v1 chain is confirmed.

**Sending less than the minimum amount of TRTL (for gas) to the service will result in the TRTL being burned and you'll receive no wTRTL or FTM as a result. You've been warned.**

# What's the maximum amount of TRTL I can wrap at once?
You can wrap up to 1,000,000,000.00 TRTL in each wrap transaction.

# Why is the amount of wTRTL I receive not exactly 100,000:1?
The gas fees for wrapping plus 0.1 FTM (sent to you) are paid in TRTL and the equivalent wTRTL is subtracted from the wTRTL equivalent of the TRTL you send in. The gas fee equivalent of wTRL is retained by us for conversion to FTM so that we keep enough FTM for the wrap service to operate.

# Why do I get 0.1 FTM from every successful wrapping transaction?
Put simply, to send transactions on the Fantom Opera Chain, you need FTM to pay gas fees. Without FTM, you'd be unable to send your wTRTL to anyone else without acquiring FTM and thus your wTRTL would be "stuck". We've made sending you 0.1 FTM part of the swap process to help prevent you from getting your wTRTL stuck.

# Do I have to wrap my TRTL?
You don't have to do it right away; however, the v1 chain is scheduled to stop at block 5,500,000 (approximately March 12, 2023, see status banner at the top of the [explorer](https://explorer.turtlecoin.ool)) so if you don't wrap by then you'll be stuck with a whole lot of nothing. Remember, there is a 60 block confirmation requirement for the TRTL you send in so do not wait until block 5,499,999 :).

# What happens to the remaining unclaimed wTRTL at the end of the wrap/swap period?
We'll burn any remaining unclaimed wTRTL by sending a transaction on the Fantom Network via the multisig Gnosis Safe.

# Seriously?
Yes.

# Can I keep mining TurtleCoin?

Yes, until the v1 chain stops at block 5,500,000.

# Are there any exchanges that support wTRTL?
Fantom Opera chain has a variety of decentralized exchanges (DEX). Below are some popular ones (not an endorsement) where you may find liquidity for exchange purposes. We'll be working on getting wTRTL whitelisted with these DEXes in the coming days/weeks.

* [SpookySwap](https://spookyswap.finance/)
* [SpiritSwap](https://www.spiritswap.finance/)

# I'm a TRTL wallet developer, can I build the wrap/swap service into my wallet?
Sure can. See the swagger docs at [https://swap-api.turtlecoin.com/](https://swap-api.turtlecoin.com/) for information on interacting with the wrap service.

# What's next for TurtleCoin?
Stay tuned for further information as wTRTL opens up a world of possibilities for the community when it comes to development of additional use cases for TurtleCoin.
