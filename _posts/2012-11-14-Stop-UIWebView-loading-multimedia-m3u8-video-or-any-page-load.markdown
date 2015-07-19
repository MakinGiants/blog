---
title: Stop UIWebView loading multimedia m3u8 video or any page load
layout: post
date: 2012-11-14 23:11:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
You have to set the html of the webview to nil:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">UIWebView *webBrowser = ...&nbsp;</code></pre><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">[webBrowser loadHTMLString:@"" baseURL:nil];  <br /></code></pre><br /><a href="http://aralbalkan.com/3326">Source</a>