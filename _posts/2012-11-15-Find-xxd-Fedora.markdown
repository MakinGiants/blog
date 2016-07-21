---
title: Find xxd Fedora
layout: post
date: 2012-11-15 02:00:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Fedora Linux
---
<br /><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;">#yum install vim-common  </code></pre><pre style="background-color: #f0f0f0; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; width: 646.4666748046875px;"><code style="word-wrap: normal;">#dd if=/dev/random bs=1 count=16 2&amp;gt;/dev/null |xxd -ps</code></pre><br /><a href="http://www.linuxquestions.org/questions/fedora-35/cant-find-xxd-for-fedora-core-5-a-459085/">Source</a>