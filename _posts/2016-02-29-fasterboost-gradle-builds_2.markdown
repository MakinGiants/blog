---
title: faster/boost gradle builds (2/2) - enjoy local cache
layout: post
categories: Android, Gradle
---

If you want to know another tip to boost gradle builds check [faster/boost gradle builds (1/2) - enjoy multiprocess]({{site.baseurl}}{% post_url 2016-02-29-fasterboost-gradle-builds %})

The idea is to have a "local" squid proxy so gradle dont have to go to get every dependency when cleaned from the web. We can have this easy with a local docker :).

I will not include a tutorial about how to install docker on mac, but its really easy :P.

1. Install [Docker hub squid](https://hub.docker.com/r/sameersbn/squid). thanks to sameersbn :)
1. Create a file `~/.gradle/gradle.properties` with the proxy settings and then all your projects will use those settings for builds.

{% gist /caipivara/f69a4bef505a3717ee88 %}

Any sugestions?