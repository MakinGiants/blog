---
title: How to wait for RxJava calls in espresso tests
layout: post
categories: Android, Testing
author: caipivara
---

Since Espresso will wait for AsyncTask to finish, we can take advantage of this 
making every RX call use the ThreadPool from there on every request, how to overrite that?

{% gist /danielgomezrico/53d0838f55cacfd030d99c64cc7b009a %}

![]( {{ site.path-emoji-tada }} )
