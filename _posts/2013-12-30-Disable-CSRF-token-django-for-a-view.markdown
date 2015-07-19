---
title: Disable CSRF token django for a view
layout: post
date: 2013-12-30 13:34:00 UTC
updated: 2015-02-08 19:42:28 UTC
comments: false
categories: Django
---
You can disable for a view adding the '<span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">csrf_exempt</span><span style="background-color: #f0f0f0; font-family: arial; font-size: 12px; line-height: 20px;">&nbsp;</span>' decorator:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> from django.views.decorators.csrf import csrf_exempt  <br />   <br /> @csrf_exempt  <br /> def my_view(request):  <br />   return HttpResponse('Hello world')  <br /></code></pre><br /><a href="http://stackoverflow.com/a/16458216/273119">Source</a>