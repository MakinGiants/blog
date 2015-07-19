---
title: Force landscape or portrait mode in application
layout: post
date: 2012-11-15 01:36:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Android
---
<br />You have to modify the activity in the "AndroidManifest.xml" adding screenOrientation in the activity properties:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> android:screenOrientation="landscape"  </code></pre><br />And thats all!<br /><br /><a href="http://stackoverflow.com/questions/2150287/force-an-android-activity-to-always-use-landscape-mode">Source</a>