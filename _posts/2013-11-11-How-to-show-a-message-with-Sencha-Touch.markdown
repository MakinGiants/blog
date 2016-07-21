---
title: How to show a message with Sencha Touch
layout: post
date: 2013-11-11 19:07:00 UTC
updated: 2015-02-08 19:42:28 UTC
comments: false
categories: Sencha Touch
---
See:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> Ext.Msg.show({  <br />      title:'Title of the message',  <br />      message: "Text of the message.",  <br />      buttons: Ext.MessageBox.OK,  <br />      fn:Ext.emptyFn  <br />    });  <br /></code></pre>