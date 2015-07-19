---
title: Count the number of string occurrences in a string NSString
layout: post
date: 2012-11-14 23:56:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<br /><div style="font-family: Menlo; font-size: 11px; margin: 0px;"><span style="font-family: Times, 'Times New Roman', serif; font-size: small;">You can replace the string that you need to search with any string and it will return the number of replaces (the number of ocurrences of the string):</span><br /><span style="font-family: Times, 'Times New Roman', serif; font-size: small;"><br /></span></div><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> int count = [baseString replaceOccurrencesOfString:@"stringToFind" withString:@"anyString" options:NSLiteralSearch range:NSMakeRange(0, [baseString length])];   <br /></code></pre><br /><span style="font-size: large;"><i><u><span style="color: red;">NOTE: Be careful, this will change the string in the baseString, so copy the string if you need to use it later.</span></u></i></span>