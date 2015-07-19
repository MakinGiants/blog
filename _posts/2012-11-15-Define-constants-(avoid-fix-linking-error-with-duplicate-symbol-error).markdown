---
title: Define constants (avoid-fix linking error with duplicate-symbol error)
layout: post
date: 2012-11-15 00:20:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS Objective-c
---
Add in header (.h) file:<br /><ol><li>Create a UNIQUE_CLASS_H identifier (this is used to avoid import link errors in compilation) BE CAREFUL: this identifier must be diferent for each .h file.</li><li>Inside de define .. add each define for each constant:</li></ol><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> #ifndef UNIQUE_CLASS_H  <br /> #define UNIQUE_CLASS_H  <br />   #define MY_STRING_CONSTANT @"Value for constant"  <br />   #define MY_INT_CONSTANT 23  <br /> #endif  <br /></code></pre><br /><b><span class="Apple-style-span" style="font-weight: normal;"><a href="http://stackoverflow.com/questions/3077426/objective-c-linking-error-with-duplicate-symbol-error" target="_blank">Source</a></span></b>