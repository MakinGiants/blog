---
title: Hide Keyboard iOS when user touch outside the textboxes
layout: post
date: 2014-07-03 20:52:00 UTC
updated: 2015-02-08 19:42:28 UTC
comments: false
categories: IOS
---
Add this code inside the ViewController:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> - (void)touchesBegan:(NSSet *)touches withEvent:(UIEvent *)event  <br /> {  <br />   // Hide keyboard if user touch the screen  <br />   [[self view] endEditing:YES];  <br /> }  <br /></code></pre><br /><a href="http://stackoverflow.com/a/15833587/273119">source</a>