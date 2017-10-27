---
layout: post
title: five minute monero
---




Getting started with Monero in 5 minutes

Monero is a cryptocurrency that tries to deliver the benefits of what we imagine a good digital cash would offer. Some of its properties include: 
	•	Total privacy of transactions.
	•	The ability to prove that you made a payment.
	•	About 2 minutes to settlement
	•	Low and predictable transaction fees, and a perpetual 1% inflation rate. 

There are no other cryptocurrencies currently available that deliver the same level of privacy and usability as Monero. But this is still a young technology, and at the moment, user-friendly wallets and other applications running on Monero are practically non-existent. If you want to start using Monero today, the only safe and usable wallet is the reference client. 

One problem is that this reference client is not as “user friendly” as people would generally expect. That’s ok, user friendly wallets are coming soon. But if you’re impatient and want to try Monero now, I’ve written a short guide here that will get you started in about 5 minutes. 

This tutorial is for OS X. 
	•	First, go to the Monero project’s download page: https://getmonero.org/downloads/
	•	Now scroll down until you see: Mac OS X, 64-bit
	•	Click Mac OS X, 64-bit (Command-Line Tools Only) and your download will start. 
	•	Go to your Downloads folder, and you’ll see this in there: (IMG)
	•	Drag that folder to your home folder like I have. Or somewhere else that’s convenient for you. (IMG)
	•	Now open your terminal. You can access it quickly in two steps: 
	◦	CMD + SHIFT to open Spotlight
	◦	Type “terminal” and then press return
	•	Your terminal window should open to your home directory. Now type “ls” and press return. If you put your Monero folder in the home directory, where I did, you should see it appear.
	•	You need to change your working directory now. Type or paste this command:  “cd monero-v0.11.1.0/“
	•	Now you can start the Monero wallet software. Paste this command: ./monero-wallet-cli --daemon-address 138.68.85.232:18089 

You are now running Monero, and hopefully this took less than 5 minutes! Since this is your first time running the wallet software, you need to create a wallet. Follow the prompts and make sure to carefully secure your mnemonic seed. 

You’ll see that your wallet starts to refresh. This should take about 2 minutes, and then you’re ready to start sending and receiving transactions. If you refresh your wallet on a regular basis, say once a day or once every few days, it should only take a few seconds to refresh your balance. The two commands that you will probably use most frequently are: 
“Address” to receive Monero

And 

Transfer {address} {amount}

To send Monero.  

Type “help” to see a full list of the commands you can use. 

If you connect to a different daemon (you used --daemon-address 138.68.85.232:18089) then this refresh could take a lot longer. This is because the computer that you are connecting to needs to be quite powerful in order to quickly process the Monero blockchain. The daemon you’re connected to here is one that I am running on Digital Ocean. here are it’s specs: 
	•	2GB RAM / 140GB storage
	•	Ubuntu 16.04.3
	•	2x CPUs

The cool thing is that using this approach is that it's just as private as running your own blockchain, because you’re not sending it any data. It just sends you some data, you see if any of it is important to you, and you discard the rest. But the downside to this approach is that I might not always be running this node- you might try to connect one day and find that I’ve taken it down. Maybe it’s become too expensive to run the node for me, or maybe I’m bored with Monero and want to do something else. Then you’d have to try connecting to some other node, and if that node doesn’t have very powerful hardware, it could take a very long time to refresh your wallet balance. You can find a list of remote nodes here: https://moneroworld.com/

The other option is to download the Monero blockchain for yourself. You’ll probably want to have at least 100GB of storage free and a fast internet connection. 


[Link to gitlab pages](https://rusticbison.gitlab.io/hcpp2017/)
