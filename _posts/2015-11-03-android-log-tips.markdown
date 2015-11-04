---
layout: post
title: "Android Log Tips"
date: "2015-11-03"
categories: Android
---

# Why

- Simple

{% highlight java %}
Timber.d["Log")
Timber.d("With some format %s and this number: %d", someString, someNumber)
Timber.e(throwable, "message")
{% endhighlight %}

- Easy setup

It will print the class name as tag and number with this setup:

{% gist danielgomezrico/a5c8197252b6db17cdd6 %}

- Helps in production release, you can set up to send all logs into crashlytics reports so you can see what was happening on users phones in this way:

{% gist danielgomezrico/18268c9963936a4e44f7 %}

# Sources

- [Jake Wharton - timber github](https://github.com/JakeWharton/timber)
- [Caster.io - episode 14](https://caster.io/episodes/episode-14-logging-with-timber/)
- [Gist 1](https://gist.github.com/danielgomezrico/a5c8197252b6db17cdd6)
- [Gist 2](https://gist.github.com/danielgomezrico/18268c9963936a4e44f7)
