---
title: Use MBProgressHUD (beauty progress bar)
layout: post
date: 2012-11-15 00:56:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Android
---
Sources:&nbsp;<a href="https://github.com/matej/MBProgressHUD">https://github.com/matej/MBProgressHUD</a><br /><div><br />Example:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> #import "MBProgressHUD.h"  <br /> // Show hud  <br /> MBProgressHUD *hud = [MBProgressHUD showHUDAddedTo:self.view animated:YES];  <br /> hud.labelText = @"Redeeming code...";  <br /> // Hide hud  <br /> [MBProgressHUD hideHUDForView:self.view animated:YES];  <br /></code></pre></div>