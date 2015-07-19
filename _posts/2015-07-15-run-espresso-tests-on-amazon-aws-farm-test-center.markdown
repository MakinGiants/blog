---
layout: post
title: "Run Espresso tests on Amazon AWS Farm test center"
date: "2015-07-15"
categories: Android
---

For [AWS Device farm](aws.amazon.com/device-farm/) you need to upload both apk, your app apk and your tests apk.

* app.apk: generated using `Build/Generate signed apk`
* test.apk: you can find it after you create a build in `/app/build/output/apk/app-debug-androidTest*.apk`. If it´s not there then you can run:

{% highlight bash %}
# ./gradlew assembleDebugAndroidTest
{% endhighlight %}

On project root.
