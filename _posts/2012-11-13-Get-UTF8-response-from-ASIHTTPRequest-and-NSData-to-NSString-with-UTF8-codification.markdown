---
title: Get UTF8 response from ASIHTTPRequest and NSData to NSString with UTF8 codification
layout: post
date: 2012-11-13 21:43:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<br /><div class="p1"><span class="s1"><br /></span></div><div class="p1">You should use the responseData instead responseString, becouse responseString use defaultCodificationString of&nbsp;<span style="background-color: white; font-family: Arial, 'Liberation Sans', 'DejaVu Sans', sans-serif; font-size: 14px; line-height: 18px;">ASIHTTPRequest.</span></div><div class="p1"><br /></div><pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><div class="p1"><br /><span class="s1">NSData</span>* data = [request <span class="s2">responseData</span>];</div><br /><div class="p2"><br />NSString<span class="s3"> *response = [</span>NSString<span class="s3"> </span>stringWithUTF8String<span class="s3">:data.bytes];</span></div><br /></pre><br /><a href="http://stackoverflow.com/a/2467856/273119">Source</a><br /><br />