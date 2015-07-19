---
layout: post
title: "How to use Espresso Contrib with Proguard and live in the try!"
date: "2015-07-13"
---

There are some conflicts on espresso dependencies so just include `com.android.support.test.espresso:espresso-contrib:2.2` with some excludes.



{% highlight groovy %}
androidTestCompile 'com.android.support.test:runner:0.3'
androidTestCompile 'com.android.support.test:rules:0.3'
androidTestCompile 'com.android.support:support-annotations:22.2.0'
androidTestCompile 'com.android.support.test.espresso:espresso-core:2.2'
androidTestCompile ('com.android.support.test.espresso:espresso-contrib:2.2'){
    exclude group: 'com.android.support', module: 'appcompat'
    exclude group: 'com.android.support', module: 'support-v4'
    exclude module: 'recyclerview-v7'
}
{% endhighlight %}

And use the proguard file:

{% highlight groovy %}

# Assertj
-dontwarn org.assertj.core.**
-dontwarn org.junit.**
-dontwarn java.beans.**
-dontwarn sun.reflect.**
-dontwarn android.test.**
-dontwarn net.bytebuddy.**
-keep class java.beans.** { *; }

-dontwarn retrofit.MockRestAdapter.**
-dontwarn rx.**
-dontwarn org.hamcrest.**

# If using retrofit
-dontwarn com.squareup.**

-keepclassmembers class java.beans.xxxx { public *; }
-keep class rx.** { *; }
-keepclassmembers class rx.xxxx { public *; }
-keepclassmembers class org.assertj.xxxx { public *; }
-keepclassmembers class org.junit.xxxx { public *; }
-keepclassmembers class java.beans.xxxx { public *; }
-keepclassmembers class android.test.xxxx { public *; }

-keepclassmembers class org.joda.time.xxxx { public *; }
-keep class org.joda.time.** { *; }

{% endhighlight %}


[Source](http://stackoverflow.com/a/30715011/273119)
