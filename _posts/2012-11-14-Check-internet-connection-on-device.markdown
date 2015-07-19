---
title: Check internet connection on device
layout: post
date: 2012-11-14 23:16:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
You need&nbsp;<a href="https://github.com/tonymillion/Reachability/blob/master/Reachability.h">Reachability code</a>&nbsp;to make it works:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> #import &lt;SystemConfiguration/SystemConfiguration.h&gt;  <br /> #import "Reachability.h"  <br /> - (bool) checkInternet{  <br />   Reachability *reachability = [Reachability reachabilityForInternetConnection];   <br />   NetworkStatus networkStatus = [reachability currentReachabilityStatus];   <br />   return !(networkStatus == NotReachable);  <br /> }  <br /></code></pre><br /><br /><div class="p3"><a href="http://stackoverflow.com/questions/1083701/how-to-check-for-an-active-internet-connection-on-iphone-sdk">Source</a><br /><div><br /></div></div><div class="p3"></div>