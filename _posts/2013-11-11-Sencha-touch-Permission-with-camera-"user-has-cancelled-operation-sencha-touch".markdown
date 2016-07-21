---
title: Sencha touch Permission with camera "user has cancelled operation sencha touch"
layout: post
date: 2013-11-11 13:59:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Sencha Touch
---
Add this permission to the list to the file "packager.json":<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> WRITE_EXTERNAL_STORAGE  <br /></code></pre><br /><i>Note: if you are using Sencha Architect you should have to edit the file with gedit or other text editor manually before build your application because Sencha Architect rewrite this file every time you save.</i>