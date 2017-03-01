---
layout: post
title: corda review
---



For some time now we’ve been hearing about R3’s secretive project, called *Corda*, which is a distributed ledger that is designed to help financial industry incumbents improve their operations. At least [one rather famous person](https://github.com/corda/corda/graphs/contributors) in the cryptofinance world has been working on it for some time, so there has been a good amount of hype surrounding it. The proof is in the pudding, so now that this thing is finally available on Github we can have a look.

![corda-logo]({{ site.baseurl }}/assets/img/corda.png){:class="img-responsive"}

Unlike many other software products and platforms in this area, it’s clear that some work has gone into this technology. The [documentation](https://docs.corda.net/getting-set-up.html) is well done and complete with working examples. The examples show that somebody worked to understand what the target audience was actually interested in and what its needs are, going a bit further than providing the typical “hello world” examples and then expecting someone else to figure out how to apply it. The commercial paper and interest rate swap examples that are provided here should be part of any demo that’s given to management and IT teams that evaluate and build applications on this technology.


- Corda is a polished, modular system that lets you create a customized, industry-specific solution
- A Corda network is meant to be private or semi-private, it’s designed to run in a trusted environment. This is designed in: all nodes in the same network have to have the same root CA certificate.
- Corda is written in Kotlin. This is a relatively new and little-used language; sold as “a better java”. This means there’s some extra cost involved in building applications. Most ambitious projects seem to be using Go or even Elixir, so this will cause some development friction. I was agitated before even trying the language: Kotlin’s homepage has a serious design flaw which prevents you from closing the cookies agreement box.
- Corda uses Oracle JVM, which is antithetical to the principles of open computing, and could lead to some interesting legal problems down the road.  
- There’s a striking similarity to the Monetas platform; Corda takes Monetas’s concepts of the Notary and network mapping in conjunction with p2p communication. Whether these are novel is perhaps questionable.
- I was surprised at how well done the documentation is, it’s complete with good examples.
- Corda uses the “Dapp" concept, which I first saw introduced by Ethereum some years ago. The key difference is that there’s no “gas” or currency in Corda, you are responsible for setting up and trusting the nodes, and figuring out how to incentivize network security and stability.


Corda is built to be very generic, and general purpose platform can be useful. But I think they’ll have trouble coming up with a compelling reason for why a company should build things on it. The key existential question inevitably arises: why should I use this technology, instead of something well known and stable such as MySQL or PSQL? What is the benefit over a permissioned database? It’s not hard to run multiple databases on different machines, and ensure they have the same information. That’s not something that can’t be done without Corda. I still don’t get it, and I haven’t found another technologist so far that has. Maybe there are some performance benefits over permissioned ledgers, but so far I have not seen any results published.  

Generally speaking, generic DLTs like Monetas, Corda, Hyperledger, and others seem to have fallen out of favor in the corporate world. I think this is because corporate clients are neither interested in nor capable of hiring and managing their own agile software development teams (or even contracting them) to build applications that run on these technologies. Apparently Digital Asset recognized this trend rather quickly, and has so far done well to abandon Hyperledger in favor of selling more specific and easily digestible “back office automation” solutions to large corporate customers. But this world of DLTs is ever-evolving, and at some point these private DLTs may be the onramp to large corporates beginning to digest real crypto assets. We’ll see how it plays out over the next year or two.
