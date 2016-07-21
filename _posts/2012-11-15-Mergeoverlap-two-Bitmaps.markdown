---
title: Merge/overlap two Bitmaps 
layout: post
date: 2012-11-15 00:40:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: Android Java
---
<br />Merge two images:<br /><br /><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;"> public static Bitmap overlay(Bitmap bmp1, Bitmap bmp2) {  <br />   Bitmap bmOverlay = Bitmap.createBitmap(bmp1.getWidth(), bmp1.getHeight(), bmp1.getConfig());  <br />   Canvas canvas = new Canvas(bmOverlay);  <br />   canvas.drawBitmap(bmp1, new Matrix(), null);  <br />   canvas.drawBitmap(bmp2, 0, 0, null);  <br />   return bmOverlay;  <br /> }  <br /></code></pre><br /><a href="http://stackoverflow.com/a/10616868/273119">Source</a><br />