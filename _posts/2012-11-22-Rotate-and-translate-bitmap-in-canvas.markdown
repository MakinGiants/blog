---
title: Rotate and translate bitmap in canvas
layout: post
date: 2012-11-22 17:19:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
Get the screen size see:&nbsp;<a href="http://www.makingiants.com/2012/11/find-display-screen-size-width-and.html">Get screen size</a><br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> float screenWidth = ...  <br /> float screenHeight = ...  <br />   <br /> Matrix matrix = new Matrix();  <br /><div class="p1"><br /> matrix<span class="s1">.</span>postRotate<span class="s1">(</span><span class="s2">accelY </span><span class="s1">*</span><span class="s2"> </span><span class="s3">10.0f</span><span class="s1">,</span><span class="s2"> </span>imageMiddleWidth<span class="s1">,</span><span class="s2"> </span>imageMiddleHeight<span class="s1">);</span></div><br /><div class="p1"><br /> matrix<span class="s1">.</span>postTranslate<span class="s1">(</span>posX<span class="s1">,</span><span class="s2"> </span>posY<span class="s1">);</span></div><br /><div class="p1"><br /><span class="s1"><br /></span></div><br />canvas.drawBitmap(bitmap, matrix, null);  <br /></code></pre><br /><br />