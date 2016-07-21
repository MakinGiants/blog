---
title: Sort array of custom objects
layout: post
date: 2012-11-13 21:34:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS
---
Implement a sort method logic in your custom class, like:<br /><br /><pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> - (NSComparisonResult)higher:(Channel *)otherChannel {  <br />     return self.number &gt; otherChannel.number;  <br /> }  <br /></code></pre><br />And then call:<br /><br /><pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> [array sortUsingSelector:@selector(higher:)];  <br /></code></pre>