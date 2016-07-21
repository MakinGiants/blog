---
layout: post
title: "Define base material colors"
date: "2015-07-02"
categories: Android 
---

Just wanted to repost a [cool post](https://plus.google.com/+AndroidDevelopers/posts/AV2ooBWY1iy)
from [IajLake](https://plus.google.com/+IanLake).

The app bar [1], or action bar, is an iconic part of many Android apps, providing a consistent place for navigation affordances and frequent, important actions. But it can also be a great opportunity to bring some personality to your app. An easy way to do that is by using your branding color as the background of the app bar.

In fact, AppCompat makes this very straightforward using a technique of providing a color palette [2] for your app. While introduced in the Material themes added in Android 5.0, AppCompat makes this technique available to all Android 2.1+ devices.

If you’re using a theme such as Theme.AppCompat, you’d only need to add a colorPrimary attribute:

{% highlight xml %}
<style name="AppTheme" parent="@style/Theme.AppCompat">
<item name="colorPrimary">@color/primary</item>
</style>
{% endhighlight %}

And your App Bar will automatically be colored appropriately. You’ll note we’re using just colorPrimary and not android:colorPrimary as android:colorPrimary only works on Android 5.0 devices unlike the AppCompat provided colorPrimary. Just make sure you’re using the right theme so that the text and icons have enough contrast:
- Theme.AppCompat -> dark activity, dark app bar
- Theme.AppCompat.Light -> light activity, light app bar
- Theme.AppCompat.Light.DarkActionBar -> light activity, dark action bar

But perhaps you’ve already moved over to Toolbars (perhaps wrapped in the Design Library’s AppBarLayout [3])? In those cases, you’re probably using a Theme.AppCompat.NoActionBar or Theme.AppCompat.Light.NoActionBar theme and including those elements in your layout XML files. Thankfully, you can still take advantage of your colorPrimary using the format ?attr/colorPrimary:

{% highlight xml %}
<android.support.v7.widget.Toolbar
android:background="?attr/colorPrimary" />
{% endhighlight %}

This ?attr/ format allows you to pull any attribute out of your theme, making it easy to consolidate your theming into a single place and avoid finding/replacing across many files.

The other thing we’ve lost is our text coloring though - there’s no Theme.AppCompat.Light.DarkActionBar.NoActionBar. Here’s where a ThemeOverlay can prove incredibly helpful. ThemeOverlays, unlike a full theme, only seek to overlay the current theme, changing the few things they need to. For example, if we had a light theme but wanted a dark Toolbar, we could use:
{% highlight xml %}
<android.support.v7.widget.Toolbar
android:background="?attr/colorPrimary"
android:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"/>
{% endhighlight %}

With just that change, our text and icons are now back to a white color - perfect for a dark Toolbar.

You’ll find a number of other colors you can and should add to your theme such as colorPrimaryDark for changing the status bar on 5.0+ devices to a darker branding color and colorAccent for a contrasting accent color designed to make elements such as a FloatingActionButton really pop out. If you’d want to learn more about AppCompat, check out our video on Consistent Design with AppCompat [4].

For now, bring some personality to your app by using colorPrimary to color your App Bar or Toolbar!

#BuildBetterApps

[1] - http://goo.gl/Meu1sE
[2] - https://goo.gl/EHaUMj
[3] - https://goo.gl/Wo1IBv
[4] - https://www.youtube.com/watch?v=5Be2mJzP-Uw﻿
