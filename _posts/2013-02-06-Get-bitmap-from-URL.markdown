---
title: Get bitmap from URL
layout: post
date: 2013-02-06 21:30:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Android
---
<div dir="ltr" style="text-align: left;" trbidi="on"><h3 style="text-align: left;"><span style="font-size: large;">Get Bitmap</span></h3><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> DefaultHttpClient httpClient = new DefaultHttpClient();  <br /> HttpGet request = new HttpGet(urlString);  <br /> HttpResponse response = httpClient.execute(request);  <br /> int statusCode = response.getStatusLine().getStatusCode();  <br />   <br /> if (statusCode == 200) {  <br />      BitmapFactory.decodeStream(response.getEntity().getContent());  <br /> }   <br /></code></pre><br /><br /></div>