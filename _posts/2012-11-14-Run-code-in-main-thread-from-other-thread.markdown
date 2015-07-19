---
title: Run code in main thread from other thread
layout: post
date: 2012-11-14 23:05:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<br /><i><br class="Apple-interchange-newline" />NOTE: To run code in the main Thread (maybe you will need to run things like UI calls from other thread...):</i><br /><div><br /><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;">  dispatch_async(dispatch_get_main_queue(), ^{  <br />       //Do things...  <br />  });  </code></pre></div><br />