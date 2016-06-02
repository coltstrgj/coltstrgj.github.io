---
layout: inner
title: 'Hybrid Crypto Research'
date: 2016-05-17 21:49:03
categories: Projects
tags: hybrid crypto
---
I recently started playing with building a hybrid cryptography system written in Go. Basically you encrypt a random symmetric key with public key cryptography after using that key to enctypt large data. This gives you the benefit of Confidentiality, Integrity (VIA signatures), and also increases the speed of the crypto by not using the slower public key crypto on the larger data. You only have to use the slow crypto for a small AES key. 

While writing this code I used it with some of the Brian Control stuff I was also working on at the time, and for safety reasons that code cannot be open sourced (yet), so the revision history is stripped, and only a simple test program is given. The test program will take input from the client terminal and send it securely to the server. Feel free to take a look at [my code](https://github.com/coltstrgj/CS-Research). It does not have a liscense at this point, so feel free to do what you like with it. 

This code is written more as a learning/research experience than a shippable product, it has lots of problems that I know about, but at the very least, the crypto should be safe. I plan on fixing some of the issues when I get a chance, and I have a few ideas that will require a backend similar to this, so those fixes may come very soon. 
