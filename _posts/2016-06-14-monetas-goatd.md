---
layout: post
title: GoatD, your Monetas wallet
---

# Background

Monetas is a peer to peer digital contracting system. You can create a contract to transfer any type of asset that is available on the system from one wallet to another, including currencies, gold grams, Bitcoin, etc. A wallet application keeps your assets on the device in which it is installed. 

# The *GoatD* wallet

There is a wallet application available for Monetas called *GoatD* that can be run on a server, or maybe your laptop. When *GoatD* is running, you can communicate with it by sending it simple HTTP requests. For example, to see your *GoatD*'s wallet balance you can use cURL to send a request:



    $ curl https://goatdplatform.monetas.io:8000/v3.0/balance

<hr class="codebreak">

    $ 200 OK
    {
      "$unit1": 124,
      "$unit2": 43
    }

There are a number of other requests you can make, such as sending 100 units:



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
* Offer wallet creation and protection service (become a bank) with a few keystrokes
* Work with other system APIs to create an exchange, for example between PayPal and Monetas
* Another exchange could be between a bank current account and Monetas

# Next steps

If you don't have *GoatD* already, the only way to get it at the moment is by becoming a corporate partner of Monetas. If you get that far, then you'll receive a download link and you can run *GoatD* from a [Vagrant](https://www.vagrantup.com/) box that uses [Virtual Box](https://www.virtualbox.org/wiki/Downloads) as a provider. The idea is that once you're a Monetas partner, it's easy to earn revenue from the transfers that come out of the applications you build.

In my next post we'll look at how to setup *GoatD* and how to create multiple wallets. Later we'll build a simple mobile wallet web app that you can turn into an iOS or Android app, or just access via a web browser. The thing to remember is that *GoatD* is your wallet, so wherever that is installed is where your money is.
