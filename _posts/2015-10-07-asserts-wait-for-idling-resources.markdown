---
title: JUnit 4 Assert wait for Espresso Idling Resource
layout: post
date: 2015-10-07 03:56:00 UTC
comments: false
categories: Android
---

Sometimes you need to wait before some async operations (maybe some EventBus or RXJava Observables) end before check something with tests, now Espresso can handle the idling resources but JUnit not.
Using [assertj-android](https://github.com/square/assertj-android) but you use  to handle async operations and tests will fail because of sync.

Example:

{% gist /danielgomezrico/df83722e4cf1fe06eb28 %}

Any suggestions?

# Resources

- [Droidcon NYC 2015 - Advanced Android Espresso](https://www.youtube.com/watch?v=GlPn60-_txk)