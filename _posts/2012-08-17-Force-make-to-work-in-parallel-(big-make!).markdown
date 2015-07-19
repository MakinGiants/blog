---
title: Force make to work in parallel (big make!)
layout: post
date: 2012-08-17 03:56:00 UTC
updated: 2015-02-08 19:42:33 UTC
comments: false
categories: Linux Programming
---
¿Are you trying to compile big projects? :)<br /><br />Use multiprocess processing to compile more faster, if you really need to.<br /><h4>Steps</h4>Replace n with the number of&nbsp;processes&nbsp;the make process will be divided.<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> $make -jn </code></pre><br /><h4>Example</h4><div>The make process will be divided in 4 subprocess.</div><div><br /></div><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> $make -j4  <br /></code></pre><br /><br /><br /><br /><i>Feel free to write your question about anything... </i>