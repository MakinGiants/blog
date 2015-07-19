---
title: Clip rounds in UIImageView (add border)
layout: post
date: 2012-11-09 04:00:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS
---
You need to add cornerRadius and maskToBounds attributes of layer:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> imageView.layer.cornerRadius = 5.0;  <br /> imageView.layer.masksToBounds = YES;  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/419472/have-a-reloaddata-for-a-uitableview-animate-when-changing">Source</a>