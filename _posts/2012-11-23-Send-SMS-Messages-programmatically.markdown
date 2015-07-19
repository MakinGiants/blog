---
title: Send SMS Messages programmatically
layout: post
date: 2012-11-23 21:12:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
Add permission to manifest: <br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> &lt;uses-permission android:name = "android.permission.SEND_SMS" /&gt;  <br /></code></pre><br />Code to send it:  <br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">  SmsManager shortMessageManager = SmsManager.getDefault();  <br />    <br />  String phoneNumber="1110001100";  <br />  String message="test text message";  <br />   <br />  shortMessageManager.sendTextMessage(phoneNumber, null, message, null, null);  <br /></code></pre><br /><i>Null parameters are message send status listeners...</i><br /><br /><a href="http://droidcoders.blogspot.com/2011/11/android-programmatically-sending-text.html">Source</a>