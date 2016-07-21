---
title: Check if NSString is null
layout: post
date: 2012-11-15 00:25:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS Objective-c
---
<pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> NSString *myString = ...  <br /> bool isNull = myString == nil || [@"" isEqualToString:myString];  <br /></code></pre><br />Now isNull variable have <i>true</i> if the string myString is null otherwise will have <i>false.</i>