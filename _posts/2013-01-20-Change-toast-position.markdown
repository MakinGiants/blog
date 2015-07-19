---
title: Change toast position
layout: post
date: 2013-01-20 03:42:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
Use setGravity<br /><br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> toast = Toast.makeText(getApplicationContext(), "This text", Toast.);  <br /> toast.setGravity(Gravity.TOP | Gravity.CENTER_HORIZONTAL, 0, 0);  <br /> toast.show();  <br /></code></pre>