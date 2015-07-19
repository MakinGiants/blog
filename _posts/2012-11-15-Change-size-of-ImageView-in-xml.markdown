---
title: Change size of ImageView in xml
layout: post
date: 2012-11-15 01:06:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Android
---
See red attributes:<br /><div style="font-family: Monaco; font-size: 11px; margin: 0px;"><br /></div><div style="font-family: Monaco; font-size: 11px; margin: 0px;"></div><pre style="background-color: #f0f0f0; background-position: initial initial; background-repeat: initial initial; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;">  &lt;ImageView  <br />         android:id="@+id/imageViewEnter"  <br />         android:layout_width="wrap_content"  <br />         android:layout_height="wrap_content"  <br /></code><code style="word-wrap: normal;"><span style="color: red;">         android:adjustViewBounds="true"  <br /></span></code><code style="color: black; word-wrap: normal;">        </code><code style="word-wrap: normal;"><span style="color: red;"> android:maxHeight="140dp"  <br />         android:maxWidth="140dp"  </span></code><code style="color: black; word-wrap: normal;"><br />         </code><code style="word-wrap: normal;"><span style="color: red;">android:scaleType="fitCenter"  </span></code><code style="color: black; word-wrap: normal;"><br />         android:src="@drawable/button_enter" /&gt;  <br /></code></pre>