---
layout: post
title: a brief introduction to the X Wallet
---




# What is the X Wallet? 
The X Wallet is a native iOS graphical user interface for the Monero reference client. The X Wallet is written in Swift, and it uses the latest libraries directly from the Monero project. You can think of the X Wallet as a GUI wrapper for the CLI, or a specialized form of the Monero GUI. The X Wallet’s marketing webpage is https://xwallet.tech/ and the source and instructions are in Gitlab.

# Can you ELI5 what the X Wallet is? 
The X Wallet is the Monero reference client packaged in a way your grandma can use. This assumes you bought her an iPhone so you could Facetime her on the weekends, like a good grandchild would.

# How does development of the X Wallet work? 
Development is being boostrapped privately. Because the software is MIT licensed, anybody can fork it and do whatever they want with it- for whatever reason they want. You’re welcome to build it now for yourself and try it out.

There are a few principles of the X Wallet project that I’ll share:
The first principle is that anybody that works on the X Wallet project gets paid, period. It might not be much, but you will get paid for your work. If the project is financially successful, then you will receive either a bonus or some sort of back payment. Nobody works for free, and every contributor receives credit.

The second is that it is best to work in really small teams. A well known principle of software development is that if you add a software developer to the project it will slow the project down, not speed it up. It takes a lot of time to review and merge code, and it’s important that everything is well reviewed before being merged.

The third is we try to deliver the highest quality work. The thought that goes into the problem that is to be solved, the quality of the system design, the code that is written, and the graphical design and UX are critically important.

# What kind of design challenges does the X Wallet face? 
It’s really difficult to deliver a consumer-grade UX when it comes to privacy oriented cryptocurrencies. Every Monero wallet today, besides the Monero reference client (and perhaps the Android wallet, but I haven’t looked into it that deeply), makes some sort of trade off where you lose most (if not all) of the privacy benefits you were expecting to receive in order to give you faster sync times and other usability benefits.

If you have already compiled the X Wallet for yourself, you know that one of the most obvious issues with the X Wallet is the sync time with the Monero blockchain. Right now we address this by connecting the X Wallet by default to an high availability setup with powerful hardware, and that helps reduce the wait time a lot when you first get setup. It’s pretty manageable, as it only takes a minute or two. But if you try to recover your wallet, get ready to wait for a long time. There are some ideas floating around for how this problem could be addressed in the future.

Another really obvious challenge in Monero is the “wait for your change” issue. Right now we address this by locking the “Send” feature of the wallet until all your change comes back. Here we have a lot of room for optimization, and we also have some ideas for how this could be done.

There are a lot of other little issues that need to be addressed, this is just a taste.
There is also a design concept we embrace which you might have already noticed: we should know absolutely nothing about you, the user.

# You fee model is stupid and I hate it! 
The X Wallet should be completely independent of any outside influence. That means it must be self-funding. Begging for funding would jeopordize the software’s ethics, and that’s not something that I will allow to happen. I believe that software should be honest and completely transparent, or it should not exist at all.

# Somebody wrote an article saying you’re compromising user privacy with your fee model. 
You can create the exact same transfer as the X Wallet by using the Monero command line interface:

`[wallet 123abc]: transfer <address> <amount> [<address 2> <amount 2>]`

A formal security audit of the X Wallet will be conducted by a professional sometime this year, if resources and luck allow. If we discover that this command does impact the overall privacy of the Monero network somehow, then we will address it at that time, and implement changes.

# Why should I use your wallet, when there are other wallets that are free?
The X Wallet is for people who appreciate Monero technology and are willing to try experimental software. If you have other motivations, you should use some other software. You should especially not use this software for anything illegal, because it is actually a honeypot.

# Trusted members of the community have said/recommended…
Don’t trust anybody.

# But they have flair on reddit and write code for the Monero project!
In that case, be extra cautious.

# The abridged recent history of the X Wallet
* Spring 2017 - I learned about monero
* Summer 2017 - I decided to create an iOS wallet for Monero. Simple personal project. No turning back now.
* Late summer 2017 - I realized people might use this software. I decided I would have to put up some money and work with professionals.
* Fall 2017 - We realized that the OpenMonero backend was going to be a lot more work than expected. Major system architecture change, here’s where the project pivoted towards no-compromises, full privacy.
* Later fall 2017 - drop a lot of planned features from v1 to try and get done by Christmas
* Sunday January 15th - Binary submitted to the App Store for approval. I publish the source code as I promised the previous summer on reddit.
* January 16- Apple rejects the app, they want to see a video of it working
* January 17 - Apple rejects the app, saying Monero is a company.
* January 18 - Apple rejects the app, ignores the additional information I provide and the give the same reason for rejection.
* January 19, morning (CET) - An anonymous author published an article titled “You shouldn’t use XWallet if you care about your privacy”. Redditors rallied against the X Wallet, calling it a scam and threat to privacy. Moderators of the Monero subreddit removed  mention of the X Wallet from the sidebar.
* January 19, afternoon - Cakewallet appears in Apple's App Store, and receives a warm reception from the Monero subreddit. Cakewallet is created and promoted by anonymous group. The software's features appear to be the same as what the X Wallet offers, but the app is closed source and it’s completely free to download and use. 
* January 19th, evening - I received an email from Apple saying someone would call me about the X Wallet’s rejection in the App Store. I have still not received a call from Apple, and the X Wallet is still blocked from the App Store.
* January 22nd - Apple has kept the app’s status as “In Review” since January 19th. Cakewallet is now highly recommended by the Monero reddit community, and some "trusted members of the Monero community" are going to work with them to ensure their software doesn't steal your Monero.

# What's next for the X Wallet?
The first objective is to get the app into the Apple App Store. This is a really weird problem, and it really appears as though Apple is playing favorites by blocking the X Wallet while at the same time welcoming Cakewallet. It's painful to start a big project and deliver it, only to discover that the people you trusted completely to be objective, fair, and independent are actually none of those things, and are actively working against you.

On the technical side of things, the focus is going to be on making progress in delivering secure and trustless software. The big goal this year is reproducible builds, which Monero itself does not have yet. Reproducible builds are crucial for ensuring that you know that the code which is running in the App Store is the same as the code which you see in Gitlab. I would also like to have at least one professional security audit conducted, which should help to ratify the quality of the product that we're offering and the claims we're making.
