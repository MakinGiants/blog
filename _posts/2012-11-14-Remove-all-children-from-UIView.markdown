---
title: Remove all children from UIView
layout: post
date: 2012-11-14 23:09:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<br />Asume that our view name is&nbsp;<span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">scrollview</span><br /><h3><span style="font-size: large;">First way</span></h3><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;"> [[scrollview subviews] makeObjectsPerformSelector:@selector(removeFromSuperview)];  </code></pre><h3><span style="font-size: large;">Second way</span></h3><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;">NSArray* subviews = scroll.subviews;  <br />for (UIView* view in subviews) {  <br />      [view removeFromSuperview];    <br />}  <br /></code></pre><br /><br /><br /><a href="http://stackoverflow.com/questions/3231399/iphone-how-to-remove-all-objects-from-a-uiscrollview">Source 1</a><br /><br /><a href="http://stackoverflow.com/questions/2123664/remove-subview-uiimageview-from-uiscrollview">Source 2</a><br />