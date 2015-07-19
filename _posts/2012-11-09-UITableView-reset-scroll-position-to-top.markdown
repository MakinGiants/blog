---
title: UITableView reset scroll position to top
layout: post
date: 2012-11-09 04:13:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS
---
You need to use <i>scrollRectToVisible</i>:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">UITableView* mainTableView...</code></pre><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">[mainTableView scrollRectToVisible:CGRectMake(0, 0, 1, 1) animated:YES];  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/724892/uitableview-scroll-to-the-top" style="background-color: white; font-family: Consolas, Menlo, Monaco, 'Lucida Console', 'Liberation Mono', 'DejaVu Sans Mono', 'Bitstream Vera Sans Mono', 'Courier New', monospace, serif; font-size: 14px; line-height: 18px;">Source</a>