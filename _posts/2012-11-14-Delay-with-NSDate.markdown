---
title: Delay with NSDate
layout: post
date: 2012-11-14 23:26:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
Use sleepUntilDate method of NSThread:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> NSDate *future = [NSDate dateWithTimeIntervalSinceNow: 2.2 ]; //In seconds  <br /> [NSThread sleepUntilDate:future];  <br /></code></pre><br /><br /><div class="p2"><h3><span style="font-size: large;">Useful links</span></h3><div><ul><li><a href="http://www.makingiants.com/2012/11/run-code-in-main-thread-from-other.html">Run code in main thread from other thread</a></li><li><a href="http://www.makingiants.com/2012/11/how-to-make-asynchronous-new-thread.html">Make asynchronous method calls</a></li></ul></div><div><br /></div><div><a href="http://stackoverflow.com/questions/1866207/how-to-use-datewithtimeintervalsincenow-fun">Source</a></div></div><div class="p2"></div>