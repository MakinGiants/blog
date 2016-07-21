---
title: Manage Git tags tutorial
layout: post
date: 2012-11-15 01:13:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Git
---
<h3><span style="font-size: large;">How to add new tag:</span></h3><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> #git tag -a TagName  <br /> #git push --tags  <br /></code></pre><br /><a href="http://book.git-scm.com/3_git_tag.html">Source</a><br /><br /><h3><span style="font-size: large;">How to remove remote tag:</span></h3><div><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> git tag -d “tag name”  //Remove the local tag either through your favorite GUI or via<br /> git push origin :refs/tags/”tag name”  //Push the removed tag to the remote origin<br /></code></pre></div><div><br /><a href="http://luismajano.com/2011/02/08/git-remove-a-remote-tag/">Source</a></div>