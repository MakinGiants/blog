---
title: How to make a Fullscreen application programmatically
layout: post
date: 2012-11-15 01:33:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Android
---
If you want to remove status bar and make full screen view add the <span style="color: red;">red code </span>in onCreate:<br /><br /><pre style="background-color: #f0f0f0; background-position: initial initial; background-repeat: initial initial; border: 1px dashed rgb(204, 204, 204); font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> public void onCreate(Bundle savedInstanceState) {  <br />  super.onCreate(savedInstanceState);   <br /> </code><code style="word-wrap: normal;"><span style="color: red;"> getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN,  <br />         WindowManager.LayoutParams.FLAG_FULLSCREEN);  <br />         requestWindowFeature(Window.FEATURE_NO_TITLE);</span></code><code style="color: black; word-wrap: normal;">  <br />      <br />  setContentView(R.layout.main);  <br /> }  <br /></code></pre>