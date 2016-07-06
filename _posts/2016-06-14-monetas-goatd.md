---
layout: post
title: GoatD, your Monetas wallet
---

# Background

Monetas is a peer to peer digital contracting system. You create contracts to transfer assets like currencies, gold grams, Bitcoin, etc. Those contracts are digitally signed and notarized, making transfers very fast, private, and ensures users can't cheat each other. A digital wallet creates and manages contracts for you.

# The *GoatD* wallet

Monetas offers a digital wallet called *GoatD* that can be run on a server, or maybe your laptop for testing and development. *GoatD* does all of the hard work of creating contracts, signing them cryptographically, etc. so that you can focus on building cool applications that make full use of the Monetas platform's capabilities. You can [download the latest version of *GoatD* here](https://goatd.monetas.net/).

When *GoatD* is running, you can communicate with it by sending it simple HTTP requests. For example, to see your *GoatD*'s wallet balance you can use cURL to send a request:



    $ curl https://goatdplatform.monetas.io:8000/v3.0/balance

<hr class="codebreak">

    $ 200 OK
    {
      "$unit1": 124,
      "$unit2": 43
    }

Make sure to modify the URL so that your port is correct and the version matches the version of *GoatD* you're using. There are a number of other requests you can make, such as sending 100 units:



    $ curl -XPOST 127.0.0.1:8000/v3.0/transfers -d '{
      "FzbrEY5ezDyHt8MADNCmfg2esrQTKDkxGiGiiQtsxn3z": {
        "568dUfJN2vXaKMGrntSsyw5pNVkTwVw34cQ677w4aMoi": 100
        }
      }'

Or retreiving your wallet's address, which is what you give to other people so they can send funds to you:




          $ curl https://goatdplatform.monetas.io:8000/v3.0/nym-id

<hr class="codebreak">

          $ 200 OK
            "$nym-id"

*GoatD* is constantly polling the Monetas Notary server to see if there's any new information available that would be of interest to you. By the way, *Goat* refers to the programming language *Go* and the *D* refers to *daemon*, because Monetas expects most users to run the application on a server. The *GoatD* daemon is built to sit in between an enterprise API, like M-PESA or PayPal (or a traditional bank), and the Monetas system. ![Interactions diagram]({{ site.baseurl }}/assets/img/interactions-diagram.png){:class="img-responsive"}

There are many interesting things that can be done with this application:

* Create a web app that is a view to *GoatD* to create and receive transfers from a mobile device or web browser
* Create permissions, so a company can use *GoatD* wallets instead of bank accounts
* Automate payroll and accounting using the same application
* Offer wallet creation and protection service (become a bank)
* Create an exchange, for example between your bank, poloniex.com or paypal.com and Monetas

# Next steps

The *GoatD* application runs in a "sandbox" environment, so you're not using real assets. The production environment hasn't launched at the time of this post, but when it's available you can simply point your *GoatD* to the production notary server. When you do that you earn a percentage of the transfer fees made with your application. Be sure to get in touch with Monetas and sign up as a partner first.  

In my next post we'll look at how to setup *GoatD* and how to create multiple wallets. Later we'll build a simple mobile wallet web app that you can turn into an iOS or Android app, or just access via a web browser. The thing to remember is that *GoatD* is your wallet, so wherever that is installed is where your money is.
