---
title: SimpleDateFormat to parse AM PM
layout: post
date: 2012-09-17 16:09:00 UTC
updated: 2015-02-08 19:42:33 UTC
comments: false
categories: Android Programming
---
If you are trying to parse an String date like:<br /><br /><i>"02:34 PM"</i><br /><i><br /></i>Init the Formatter with US locale:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> SimpleDateFormat("hh:mm a", Locale.US);  </code></pre><span class="s1"><br /></span><span class="s1"><i>Note: Witouth the locale parameter it say "Parse failure" error message.&nbsp;</i></span><br /><i><br /></i>