---
title: UITableView reload data with animation
layout: post
date: 2012-11-09 04:02:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: IOS
---
Call <i>reloadSections:withRowAnimation</i>&nbsp;metod from UITableView object:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">[myTableView reloadSections:[NSIndexSet indexSetWithIndex:0]&nbsp;</code></pre><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">           withRowAnimation:UITableViewRowAnimationTop];  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/419472/have-a-reloaddata-for-a-uitableview-animate-when-changing">Source</a>