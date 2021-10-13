---
layout: "post"
title: "Introducing CryptoNight Soft Shell"
description: "Introducing CryptoNight Soft Shell TurtleCoin Aug 14, 2018 · 5 min read Objective To provide the next generation PoW algorithm for TurtleCoin that..."
image: "{{ site.baseurl }}/images/0u3c3AOOzcsVNkK6y"
date: "2018-08-14T02:08:55.755Z"
---

# Objective

To provide the next generation PoW algorithm for [TurtleCoin](https://turtlecoin.lol/) that accomplishes the following goals:

- Must be a PoW that is different than any other PoW algorithm deployed by another blockchain.
- Provides additional ASIC/FPGA resistance
- Encourages solo-mining for decentralization of hashrate
- Uses a variable amount of of resources (CPU & Memory) that changes dynamically as the chain progresses.
- Helps to stablize hashrate over time

# Problem

Typical implementations of the CryptoNight slow hash routines require static resource amounts to complete the hash calculations.

The figure below is provided for illustrative purposes.

![]({{ site.baseurl }}/images/0m79ILq_xVKRojKW3)

Developers typically jump between any of the resource levels presented by the PoW algorithms or create slight variations of those algorithms to define new resource requirement levels for generating PoW hashes. What fun is that though?

# NERVA

As @angrywasp explains in the interview [CN Adaptive, Nerva, and the Quest For Fair Mining](https://blog.turtlecoin.lol/archives/cn-adaptive-nerva-and-the-quest-for-fair-mining/) they approach this issue by changing the PoW every block with CN-Adaptive. This provides a resource requirement that changes over time.

The figure below is provided for illustrative purposes.

![]({{ site.baseurl }}/images/0CsGyzGVLDrsd1cbw)

As you can see, the line is not straight like normal CryptoNight variants. This change is provided by altering the number of iterations the slow hash algorithm performs in relation to the chain height. They do this in the following way (see [permalink](https://github.com/blockchain-research-foundation/nerva/blob/27527fc212f8cc70ceeb2310a1630aee45883cb7/src/cryptonote_basic/cryptonote_format_utils.cpp#L892)). This variation is enough that it makes it harder to implement specialized hardware to mine this PoW algorithm.

![]({{ site.baseurl }}/images/0NhisWgYTMm9VN4ZY)

Let’s break this down with some sample math. Don’t worry, I’ll keep this simple.

We’ll use an example height of `10,000` to make things easy.

1. We take `height` and add `1` to it giving us `10,001`.
2. We then perform a [modulo operation](https://en.wikipedia.org/wiki/Modulo_operation) on the values such that `10001 % 1024`and get the result `785`.  
   **Note:** A modulo operation is a division operation that returns just the remainder.
3. The result of #3 is fed to a simple addition operation that adds the value to either `0x40000` (262144) or `0x80000` (524288) arriving at the result `262929`.
4. That value, `262929` is then fed to the slow hash routine as the number of iterations to perform.

NERVA creates a [Sawtooth](https://en.wikipedia.org/wiki/Sawtooth_wave) that climbs a hill that at it’s peak increases the iterations performed by 1,023\. Zooming in, it might look something like this:

![]({{ site.baseurl }}/images/0QzO4ri8pb-saN4rW)

The work NERVA is doing is interesting and got us thinking… if they can change the iterations… what happens when we go crazy?

# CryptoNight Soft Shell

![]({{ site.baseurl }}/images/0u3c3AOOzcsVNkK6y)

Being a Turtle has it’s advantages at times, we’re slow, steady, reliable, and like to do things our own way. As such, our buddy @iburnmycd has created a variation of the PoW that is complex enough to meet the requirements above and provides an interesting resource utilization curve.

Instead of a flat (or nearly flat) resource utilization curve CryptoNight Soft Shell has a curve like this:

![]({{ site.baseurl }}/images/0odPx5efib9ruymjc)

How do we do this? To put it simply, we vary both the iterations and the [scratchpad memory](https://en.wikipedia.org/wiki/Scratchpad_memory) used in such a way that we move from what we’ll call CryptoNight Ultra Fast all the way up past CryptoNightv7 and then cycle back around again to CryptoNight Ultra Fast. One full cycle is completed every 4,096 blocks (and is highly configurable).

We still use height as the foundation of how the math is performed as it is something that we can all easily agree upon. The resulting code looks something like this (subject to change and protected under GPLv3).

![]({{ site.baseurl }}/images/00oCb9MnNmpbV42FZ)

Changing just one of the initial defitions drastically changes the results.

If we change the `CN_SOFT_SHELL_WINDOW` to `1024` our cycle looks something like this:

![]({{ site.baseurl }}/images/0npYim4EFgoXQBVaC)

If we change the `CN_SOFT_SHELL_MULTIPLIER` to `1` our cycle looks something like this:

![]({{ site.baseurl }}/images/0mihsFjvgZIGxSUfd)

Or change the `CN_SOFT_SHELL_MULTIPLIER` to `16` our cycle looks something like this:

![]({{ site.baseurl }}/images/0myTX9xfaUTQW_Jc9)

Or we can have a little bump here and there by changing `CN_SOFT_SHELL_MULTIPLIER` to `16` and `CN_SOFT_SHELL_WINDOW` to `512`

![]({{ site.baseurl }}/images/089j2GMf1dnfs6sYl)

The options are practically endless in how the PoW algorithm can be altered.

# Hashrate Variance

A by-product of CryptoNight Soft Shell is that a miner’s hashrate moves according to where in the cycle the blockchain is as the algorithm itself changes over time. This means that as the blockchain reaches the peak of the given cycle, a miner’s hashrate slows. Then, as it starts to return back to the lower valley of the curve, a miner’s hashrate speeds up very fast.

# Difficulty Variance

One problem with a Sawtooth Wave is that if the peak of the wave is too far off from the bottom it becomes possible that a mining difficulty adjustment is required otherwise the first few blocks of any given cycle may come out very fast or in some situations very slow. Unlike a Sawtooth Wave, CryptoNight Soft Shell climbs and falls in a safe way. Each step is clearly defined throughout the entire cycle. This helps protect network difficulty from sudden changes as a result of the mining resource utilization rising and/or dropping with each block.

# Questions? Comments?

Given the choice, which PoW algorithm looks like the most fun to you?

![]({{ site.baseurl }}/images/0XzZp5lw7Z5YM5fj4)

Hit us up on Discord at [http://chat.turtlecoin.lol](http://chat.turtlecoin.lol/) in the #dev_general channel to learn more.
