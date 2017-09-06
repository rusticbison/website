---
layout: post
title: evolution of cryptocurrencies
---



As cryptofinance has evolved over the last few years, I've observed a few trends that I think provide a general indication of things to come. Here are a few observations I've made regarding the ongoing development of cryptofinance.


## Single currency systems are not naturally occurring
Who wants to deal with exchanging the Forint, the Franc, the Deutschmark, and the Pound on a single business trip? Why can't we all just agree on one trade instrument, so I don't have to deal with all that change in my pocket? In 2014 I imagined that people liked using the US dollar and the Euro because having a single currency made trade easier. I also imagined that a unified, borderless currency like Bitcoin would eventually be preferred to multiple currencies. But this is definitely not how things work.

But it turns out that currencies like the US Dollar and the Euro are more or less artificially imposed on people, they are not naturally occurring. The reality is that [Dunbar's number](https://en.wikipedia.org/wiki/Dunbar%27s_number) leads humans to naturally cooperate in a more fragmented, tribal way. We can see this behavior now very clearly in cryptocurrencies. In Bitcoin, we see that people with slightly different interests will not cooperate, but will separate and "fork" Bitcoin, to give it the nuanced properties they desire. Both groups continue to trade with each other. The objective usefulness of the new cryptocurrency's properties (or lack thereof) doesn't matter. What matters is that we can see how groups fragment as they get larger, and they tend to prefer to create their own cryptocurrencies, yet still trade freely with each other.

I reference here Nick Szabo's concept of [http://unenumerated.blogspot.com.ee/search?updated-max=2017-02-23T23:48:00-08:00&max-results=11](social scalability).


## Some cryptocurrencies can be traded completely peer to peer
The way we trade cryptocurrencies today is by trusting third party intermediaries that operate exchange businesses. But this is a serious problem, because exchanges can:
* create fake volume
* front run or otherwise trade against customers
* discriminate against customers
* steal customer funds

We can also trade cryptocurrencies peer to peer, but in the simplest case we have to fully trust our trading partner. For example, suppose Alice has Bitcoin, and Bob has Zcash. They can work out a deal on the phone; Alice will send 1 Bitcoin to Bob, and in exchange Bob will send 1 Zcash to Alice. The problem is that Bob will be tempted to cheat after he receives Alice's Bitcoin; there is no recourse if he does not follow through on his promise to send Alice his Zcash.

But Bob can be incentivized to follow through on his trade obligation, using a technique called [atomic cross chain trading](https://en.bitcoin.it/wiki/Atomic_cross-chain_trading), which was first proposed by [TierNolan in 2013](https://bitcointalk.org/index.php?topic=193281.msg2224949#msg2224949).

This technique has already been demonstrated by researchers using [Zcash and Bitcoin](https://github.com/zcash-hackworks/zbxcat), but it could also be done between any two cryptocurrencies that support simple contract and time lock features. The user would need to run both clients, as well as a "middleware" client that handles all of the logic.


## Mutually Assured Destruction is useful in commerce
This is trickier in practice than trading two cryptocurrencies. But we can use game theory to incentivize buyers and sellers of merchandise in a way that works fairly well most of the time. For example, a seller of an item that is priced at 1 XMR might have to commit collateral of 1 XMR to a trade, while the buyer agrees to pay 1 XMR but must also commit 1 XMR as collateral. If either party defaults, the total collateral is forfeited. This doesn't work well for genuine "lost in the mail" situations, but if the delivery service's tracking system is trustworthy enough to be used as an oracle, then a fairly robust system can be built.


## Conclusion: Moon bound
I think that we'll see two big trends emerge in the next few years, which will be driven by catastrophic failures of memecoins (including fiat currency) and third party exchanges and intermediaries.

1. High quality cryptocurrencies will be traded atomically (and vice-versa) and companies that operate exchanges will be relegated to listing low quality cryptocurrencies. Atomic swap price data will emit the only trustworthy price data.
2. Peer to peer online markets will become consumer friendly. Bisq is an early example of a working p2p marketplace, but it's just not ready for most people to use. I can see integrations with XBT and XMR coming in the near future.
