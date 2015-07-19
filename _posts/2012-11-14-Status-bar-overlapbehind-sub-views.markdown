---
title: Status bar overlap/behind sub views
layout: post
date: 2012-11-14 20:58:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<br /><ol><li>Use the next line after adding the subview:</li></ol><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> self.view.window.rootViewController.view.frame = [UIScreen mainScreen].applicationFrame;  </code></pre><br /><br /><div><ol><li>Write in application delegate:</li></ol></div><div><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;"> viewController.view.frame = window.screen.applicationFrame;  <br /> [window addSubview: viewController.view];  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/487150/uiview-clipped-by-statusbar-until-autorotate">Source 1</a></div><br /><a href="http://stackoverflow.com/a/11292234">Source 2</a>