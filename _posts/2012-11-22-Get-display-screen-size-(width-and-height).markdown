---
title: Get display-screen size (width and height)
layout: post
date: 2012-11-22 16:05:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
From an activity:  <br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> Display display = ((WindowManager)getSystemService(Context.WINDOW_SERVICE)).getDefaultDisplay();  <br /> float screenWidth = display.getWidth();  <br /> float screenHeight = display.getHeight();  <br /></code></pre>