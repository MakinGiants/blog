---
title: How to check null/empty string in javascript
layout: post
date: 2013-11-04 18:25:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Javascript
---
<pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> if(/[^\s]+/.test(title)){  <br />   //Is not empty  <br /> }else{  <br />   //Is empty  <br /> }  <br /></code></pre>