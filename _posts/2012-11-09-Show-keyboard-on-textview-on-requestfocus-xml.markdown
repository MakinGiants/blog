---
title: Show keyboard on textview on requestfocus xml 
layout: post
date: 2012-11-09 21:32:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: Android
---
<div>If you want to request focus and show keyboard when a view is loaded you should do:</div><ul><li>Into the EditText XML add &lt;requestFocus/&gt; tag:</li></ul><div><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">   &lt;EditText&gt;  <br />      ...  <br />      &lt;requestFocus /&gt;  <br />   &lt;/EditText&gt;  <br /></code></pre></div><ul><li>In the Application Manifest add the property "windowSoftInputMode":</li></ul><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">   &lt;activity  <br />    ...  <br />   android:windowSoftInputMode="stateAlwaysVisible"/&gt;  <br /></code></pre><br /><a href="http://stackoverflow.com/questions/1509719/android-how-to-make-the-keypad-always-visible">Source</a>