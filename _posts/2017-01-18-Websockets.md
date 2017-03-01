---
layout: post
title: websockets
---

I spent some time today considering different ways to provide realtime data to visitors of a web site, and ultimately decided the requirements were best met by websockets. The web seems to be a wasteland when it comes to knowledge on websockets, but fortunately I discovered some very helpful code snippets provided by [BTCthreads](http://btcthreads.com/display-real-time-bitcoin-transactions-with-jquery-and-websocket/).

![debug-screenshot]({{ site.baseurl }}/assets/img/debug.png){:class="img-responsive"}  

# About

A relatively new ([2008](https://en.wikipedia.org/wiki/WebSocket)) technology, websockets are a very interesting and powerful tool. Websockets provide big reductions in latency as well as the amount of data transmitted over other TCP/IP methods.
