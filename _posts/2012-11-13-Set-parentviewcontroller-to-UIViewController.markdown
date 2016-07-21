---
title: Set parentviewcontroller to UIViewController
layout: post
date: 2012-11-13 21:39:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS
---
Call setValue:forKey: and use key _parentViewController with the viewController:<br /><br /><pre style="background: none repeat scroll 0% 0% rgb(240, 240, 240); border: 1px dashed rgb(204, 204, 204); color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> - (void)setParentController:(UIViewController*)parent{  <br />   [self setValue:parent forKey:@"_parentViewController"];  <br /> }  <br /></code></pre><br /><a href="http://stackoverflow.com/a/2802654/273119">Source</a><br /><br />