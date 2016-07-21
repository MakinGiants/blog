---
title: Parse char to int (get ASCII or int value)
layout: post
date: 2012-11-14 23:22:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS Objective-c
---
<h3><span style="font-size: large;">Get ASCII value</span></h3><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> char c = 'A';  <br /> int x = (int)c;</code></pre><br />Now x is equal to 65 (ASCII code of char 'A')<br /><h3><span style="font-size: large;"><br /></span></h3><h3><span style="font-size: large;"><br /></span></h3><h3><span style="font-size: large;">Convert '1' char to 1 int value</span></h3><div><i>Only works with chars '0' - '9'</i><br /><br /></div><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> char c = '1';   <br /> int x = (int)(c - '0');  <br /></code></pre><div><br /></div><div>Now x is equal to 1</div><br /><br /><br /><br />&nbsp;<a href="http://www.iphonedevsdk.com/forum/iphone-sdk-development/12793-how-convert-char-int.html">Source</a>