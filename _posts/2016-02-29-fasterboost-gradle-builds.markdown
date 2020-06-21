---
title: faster/boost gradle builds (1/2) - enjoy multiprocess
layout: post
categories: Android, Gradle
---

Check if you want to know more tips check [faster/boost gradle builds (2/2) - enjoy local cache]({{site.baseurl}}{% post_url 2016-02-29-fasterboost-gradle-builds_2 %})

You can create a file `~/.gradle/gradle.properties` and then all your projects will use those settings for builds.

My local machine setup: 
- MacBook Pro (13-inch, Mid 2012)
- core i5: 4 (4+1 threads will be great for builds)
- ram: 16 GB 1600 MHz DDR3.

{% gist /danielgomezrico/50de23e3fc75f521ada5 %}

Thanks to [Reddit](https://www.reddit.com/r/java/comments/22rb8z/gradle_build_process_is_painfully_slow/)

Any sugestions?