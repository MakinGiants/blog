---
title: Resolve ListView Scrolling background color goes to black
layout: post
date: 2012-11-09 21:16:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: Android
---
You must set the cacheColorHint color to transparent.<br />You can do it in two ways:<br /><ul><li>Add into xml definition:</li></ul><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> android:cacheColorHint="@android:color/transparent"  <br /></code></pre><ul><li>Programmatically:</li></ul><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> setCacheColorHint(Color.TRANSPARENT);  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/3011945/scrolling-a-listview-changes-everything-from-white-to-black">Source</a>