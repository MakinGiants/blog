---
title: How to show message alert
layout: post
date: 2012-11-15 00:00:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> UIAlertView *alert = [[UIAlertView alloc] initWithTitle:@"Title of the   message"  <br />   message:@"message to show"  <br />   delegate:nil   <br />   cancelButtonTitle:@"OK"   <br />   otherButtonTitles:nil];[alert autorelease];  <br /> [alert show];  <br /></code></pre><br /><a href="http://www.ios-developer.net/iphone-ipad-programmer/development/alert-view/message-box-action-sheet-general">Source</a>