---
title: Fix Safari invalid URL in authorization error with ShareKit
layout: post
date: 2012-11-13 21:46:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
In Facebook.m<br /><br />Change:<br /><br /><pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> [self authorizeWithFBAppAuth:YES safariAuth:YES];  <br /></code></pre><br /><span class="s1">To:</span><br /><span class="s1">&nbsp;</span><br /><div class="p1"><span class="s1">  <pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> [self authorizeWithFBAppAuth:NO safariAuth:YES];  <br /></code></pre></span></div><br /><a href="http://stackoverflow.com/questions/8851639/sharekit-2-problems-with-connecting-to-facebook-after-user-authentication">Source</a>