---
title: Fix ICS Plugin not listed in LiveView Application and LiveView Clock Devel 
layout: post
date: 2012-11-04 23:20:00 UTC
updated: 2015-02-08 19:42:32 UTC
comments: false
categories: Android LiveView
---
If you install the sandbox plugin in ICS and it is nos listed in the plugins list and in the Clock you should add an <i><span style="color: red;">action (see red action in next code)</span></i>&nbsp;into the intent-filter of your <i>Android Plugin Manifest:</i><br /><br />Your intent filter of the plugin service must look like:<br /><br /><pre style="background-color: #f0f0f0; background-position: initial initial; background-repeat: initial initial; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">&lt;intent-filter&gt;  <br />         &lt;action android:name="com.sonyericsson.extras.liveview.plugins.sandbox.sandboxpluginservice" /&gt;  <br />         &lt;category android:name="android.intent.category.LAUNCHER" /&gt;  <br /></code><code style="word-wrap: normal;"><span style="color: red;">         &lt;action android:name="android.intent.action.MAIN" /&gt;  <br /></span></code><code style="color: black; word-wrap: normal;">&lt;/intent-filter&gt;  <br /></code></pre><br /><a href="http://omgwtfgames.com/2012/08/fix-missing-plugins-for-sony-liveview-android-4/">Source</a>