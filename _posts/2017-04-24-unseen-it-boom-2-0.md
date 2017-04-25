---
layout: post
title: the next (silent) internet boom
---



I sent my first email in 1995, and built my first webpage in 1998. It was a simpler time for web development, you could write some basic HTML with the styling in-line, and then host it on your own machine and try to keep your computer from crashing so people could access it.

A lot has changed in 20 years. Today we're building web applications, full computer programs that people interact with through their web browser. The complexity of these systems has increased dramatically over time. Consider the web application I'm currently building and deploying:


- it begins as a full python computer program

- a framework called Flask helps it become a web application, serving resources like...

- images, HTML and CSS, but also scripts that run in your browser, like javascript and jquery

- something called server sent events lets my server program connect to and update your browser in realtime

- an application that runs on my server called Celery uses multithreading technology to run "workers" on my server in the background, so my python program can do things like check a stock ticker price from another server and update your browser with the current price

- a server application called gunicorn for deploying Flask

- an application called supervisor makes sure all of these things are running, and if they crash then it restarts them

- and NGINX is the web server that finally connects all of this to your browser


If we pull all of this together, we can access Poloniex.com's API to check the current price of Bitcoin: http://xbtdata1.com/

It seems like a lot of work. But once this software foundation is in place we can do some really spectacular things. If we simply add a Bitcoin client to the server we can create much simpler user interface for payments, so it's easier for customers to buy our products and services and we don't lose so many during the "checkout" process everyone despises. That's the next feature I'll be adding to this application, which I'll discuss in an upcoming post. 
