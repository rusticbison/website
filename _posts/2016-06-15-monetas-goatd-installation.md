---
layout: post
title: simple installation and configuration guide for the GoatD wallet
---

# Background

Monetas is a peer to peer digital contracting system. You can create a contract to transfer any type of asset that is available on the system from one wallet to another, including currencies, gold grams, Bitcoin, etc. In my last post I introduced *GoatD* and presented some ideas for what you could do with it. Today we'll get our hands dirty as we install and configure the version of *GoatD* that comes in a Vagrant package. The instructions for the binary alone are [packaged with the binary tarball](https://goatd.monetas.net/).

# *GoatD* installation

Add the vagrant box to your vagrant using following command:

    $ vagrant box add goatd-1.0.93.box --name goatd-1.0.93

Initiate vagrant system in chosen directory:

    $ vagrant init

Open and edit Vagrantfile, change: config.vm.box ="base" TO config.vm.box = "goatd-1.0.93". Start vagrant box:

    $ vagrant up

Login to Vagrant:

    $ vagrant ssh

Login as root:

    $ sudo su -

Create a new wallet:

    $ newwallet

You will see this output after running the *newwallet* script:

    ==========================
    = NEW WALLET INFORMATION =
    ==========================

    Wallet SK:  5PVC93gPAXj3hWUoDsVVda5E3fs8smp2ZCbWCc2g6Zqw....
    Wallet port:  53968
    Wallet service:  rungoat-5PVC9
    Wallet identifier:  5PVC9

Notice that you can run the *newwallet* script as many times as you like; each time a new Monetas wallet is being generated, with a new port for you to communicate with it.

I've packaged the current version of *GoatD* with a simple Python script that helps you easily make requests to *GoatD*, I call it *goatease*. To try it, first open *goatease.py* in Vim, then copy the port of your new wallet and then paste it in place of *XXXXX* in the following string:

    url=('http://127.0.0.1:XXXXX/v3.0/')

Now save goatease.py and run it:

    $ ./goatease.py

<hr class="codebreak">

    Press 'a' to see your wallet address and generate a QR code.
    Press 'b' to see your balance.
    Press 'u' to see units available on the Notary.
    Press 's' to see the status of a pending transfer.
    Press 'n' to create a new transfer.'
    Press 'f' to see the fees for a particular unit.
    To quit, press 'q'.

# Next steps

Today we installed *GoatD*, configured it, and learned how to create multiple wallets on the same virtual machine. We also ran a simple script that makes sending simple HTTP requests to *GoatD* easy. Next time we'll build a simple mobile wallet web app that you can turn into an iOS or Android app, which will let you do the same things that *goatease.py* does.
