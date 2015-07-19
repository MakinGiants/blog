---
title: Antialias with matrix transformation in bitmap
layout: post
date: 2012-11-22 18:58:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
Your image change it resolution when you use Matrix and transform it?<br /><br />Use a Paint and setFilterBitmap and setAntiAlias to true and thats all, you bitmap colors will not going to be changed at all...<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> Paint paint = new Paint();  <br /> paint.setAntiAlias(true);  <br /> paint.setFilterBitmap(true);  <br /> canvas.drawBitmap(bitmap, matrix, paint);  <br /></code></pre><br /><a href="http://stackoverflow.com/a/4846130">Source</a>