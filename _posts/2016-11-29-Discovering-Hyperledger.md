---
layout: post
title: Discovering Hyperledger
---

After hearing a bit about Hyperledger, I decided to investigate further and see if this thing might be useful, and if so, where.  

![hyperledger-logo]({{ site.baseurl }}/assets/img/hyperledger-logo.png){:class="img-responsive"}  

# About Hyperledger

The first thing to know about Hyperledger is that it is not actually software, it's a project framework that's being administered by the Linux foundation. If you come up with a blockchain thing that you think is good for one reason or another, you submit a proposal to the Linux foundation and if it is approved, your blockchain thing goes into 'incubation' in the Hyperledger project. The full details for how this works are written out [here](https://wiki.hyperledger.org/community/project-lifecycle).

The idea is that if you're building a new blockchain thing, it makes life easier for everyone involved if all the software is written with some generally accepted programming standards in mind, and that's what this project framework is supposed to enforce. The idea is code *interoperability*. This makes sense, and they at least have a project charter, so that's good. The next step is to have a look at what blockchain(s) are actually available to go to work...

# Three blockchains

The short answer is "none". That's disappointing, given how much interest is out there. But, there are three blockchains that are just past the proposal stage:

- Fabric (IBM)
- Iroha
- Sawtooth Lake (Intel)

Of the three blockchains available, Fabric seemed to be the easiest to get started with; the dependencies are familiar and documentation seems fairly well done, although their Slack user group seems to have a lot more questions than answers.

 >A really important point to emphasize: *none of these blockchains are interoperable, at all*. Just like any other blockchain today, you'd have to use some third party service to swap contracts or tokens across blockchains. The best example of this that I can think of is [Shapeshift.io](https://shapeshift.io), which works very well.

I was able to get started with Fabric without any problems at all, it was a very smooth process on a Mac. But that's where it ends. From an outsider's perspective, there's no working example application that runs on these rails, there aren't any diagrams that could explain how things work, and you're really just left wondering why you wasted your time setting this thing up.  

# Applications

The most fundamental test case for all blockchain technologies is how they handle a cryptocurrency or token. After my experience with Fabric, I'm not going to spend time on the other blockchains that Hyperledger offers, because none of these even present a working application that can be used for benchmarking. I have no doubt that the other two blockchains (Iroha and Sawtooth Lake) are less developed.

It's entirely possible I haven't dove deep enough, and there are really amazing things waiting for me if I dive deeper. But I'm exploring from a business context, and in business time is money. So here's the conclusion: if you have a ton of money and just want to be able to say you have a blockchain project and you need some prestige, pay IBM or Intel to build software for you using one of their blockchains. If you need rails that are ready to go right now for a serious business application, you'll need to build your application on Bitcoin or Ethereum.
