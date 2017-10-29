---
layout: post
title: Five minute monero
---




Monero is a cryptocurrency delivers the benefits of what we imagine a good digital cash might offer. Some of its properties include: 

* Total privacy
* The ability to prove that you made a payment
* About 2 minutes to settlement
* Low and predictable transaction fees, and a perpetual 1% inflation rate 

There is no other cryptocurrency currently available that deliver the same level of privacy and usability as Monero. 

At the moment there's only one trustworthy and reliable wallet for Monero, and that's the official wallet that the Monero project developers maintain. The problem is that this wallet isn't as user friendly as many people would have hoped. So I’ve written a short guide here that will hopefully get you started with Monero in about 5 minutes. 

This tutorial is for OS X, but the general process is the same for other operating systems.

* First, go to the Monero project’s download page: https://getmonero.org/downloads/
* Now scroll down until you see: Mac OS X, 64-bit
* Click Mac OS X, 64-bit (Command-Line Tools Only) and your download will start. ![download-monero]({{ site.baseurl }}/assets/img/monero-tutorial/download-monero.png =250x){:class="img-responsive"}
* Go to your Downloads folder, and you’ll see the binary file you just downloaded in there. Double cick it, and it should unzip. You should see something like this: ![monero-extracted]({{ site.baseurl }}/assets/img/monero-tutorial/monero-extracted.png =250x){:class="img-responsive"}
* Drag (which means copy) that folder to your home folder: ![monero-at-home]({{ site.baseurl }}/assets/img/monero-tutorial/monero-at-home.png =250x){:class="img-responsive"}
* Now open your terminal. You can access it quickly in two steps: 
* CMD + SHIFT to open Spotlight
  - Type “terminal” and then press return
* Your terminal window should open to your home directory. Now type “ls” and press return. If you put your Monero folder in the home directory, where I did, you should see it appear. ![terminal-ls]({{ site.baseurl }}/assets/img/monero-tutorial/terminal-ls.png =250x){:class="img-responsive"}
* You need to change your working directory now. Type or paste this command:  “cd monero-v0.11.1.0/“
* Now you can start the Monero wallet software. Paste this command into your terminal window: ./monero-wallet-cli --daemon-address 138.68.85.232:18089 

You are now running Monero!

![monero-boot]({{ site.baseurl }}/assets/img/monero-tutorial/monero-boot.png =250x){:class="img-responsive"}

Since this is your first time running the wallet software, you need to create a wallet. Follow the prompts and make sure to carefully secure your mnemonic seed.

You’ll see that your wallet starts to refresh. This should take about 2 minutes, and then you’re ready to start sending and receiving transactions. If you refresh your wallet on a regular basis, say once a day or once every few days, it should only take a few seconds to refresh your balance. The two commands that you will probably use most frequently are "address" and "transfer". The first is:

```bash
address
```

which displays your own address. Use this to receive Monero. You'll also like:  

```bash
transfer {address} {amount}
```

To send Monero. Just replace {address} with the address you want to send Monero to. Replace {amount} with the amount of Monero you want to send. You might enter "0.5", for example.

Here's the full command:

```bash
transfer 42QAjkkawAAP2L2tr2aZ2QFWgMD8TS4Q14d4QPXANDpyexWrFBrnECsMYmnxAZhMoX8ZoAJ6YCnPLgmxe8HCFxpo7BBJ87Z 0.5
```

You'll be asked to enter your password to confirm the transfer. There are many other commands available, besides just "address" and "transfer". Type "help" to see all of them. The cool thing is that when you use this "remote node" approach you don't lose any privacy at all. The daemon sends your wallet some data, your wallet checks to see if any of it is important to you, and then it discards the rest. Nothing important leaves your computer, so even if the remote node operator were evil and wanted to spy on you, they couldn't.

Any server that runs the Monero daemon is called a remote node. There are three considerations when using a remote node:
1. Speed. If the remote node is receiving a lot of traffic or doesn't have much memory or CPU power available, it will take your wallet longer to refresh.
2. Bandwidth. Make sure you've got a fast connection!
3. Availability. The node you're connecting to might be down. Maybe the person operating it got bored with Monero, or it became too expensive to operate. You can look for other remote nodes that you can connect to here: https://moneroworld.com/

If you followed my instructions, you connected to a remote node that I operate. it is a Virtual Private Server from Digital Ocean. Here are it’s specs: 

	•	2GB RAM / 140GB storage
	•	Ubuntu 16.04.3
	•	2x CPUs

Let me know if you have any trouble connecting to my remote node, or if it is taking more than a few minutes to refresh your wallet.


[Link to gitlab pages](https://rusticbison.gitlab.io/hcpp2017/)
