---
title: Create a translate animation
layout: post
date: 2012-11-15 00:48:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: Android
---
Create a TranslateAnimation object, set animation prefs and set it to View object (in this example&nbsp;<span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">myView)</span><br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> TranslateAnimation animation = new TranslateAnimation(Animation.RELATIVE_TO_SELF,   <br /> 0.0f,Animation.RELATIVE_TO_SELF, 0.0f,Animation.RELATIVE_TO_SELF,   <br /> 1.0f,Animation.RELATIVE_TO_SELF, 0.0f);  <br /> animation.setDuration(700);  <br /> animation.setInterpolator(new OvershootInterpolator());  <br /> myView.startAnimation(animation);  <br /> <span style="font-family: arial;">myView</span></code>.setVisibility(View.VISIBLE);  </pre><br />Note:&nbsp;<span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">myView</span>&nbsp;can be any layout or a view