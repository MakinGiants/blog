---
title: Show a Select Field inside a MessageBox Sencha Touch 2.x
layout: post
date: 2014-01-22 16:31:00 UTC
updated: 2015-02-08 19:42:28 UTC
comments: false
categories: Sencha Touch
---
<pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> Ext.Msg.prompt(  <br />   'Test',  <br />   'Open the picker',  <br />   function(buttonId, value) {},  <br />   me, //scope  <br />   false, //multiline  <br />   0, // default  <br />   { // prompt config  <br />     xtype: 'selectfield',  <br />     displayField: 'value',  <br />     store: 'SettingsTag',  <br />     usePicker:false  <br />   }  <br /> );  <br /></code></pre><br /><br /><a href="http://try.sencha.com/touch/2.0.0/demos/Ext.field.Select.usePicker/">Source</a><br /><br /><a href="http://try.sencha.com/touch/2.2.0/demos/Ext.field.Select.showPicker/">Source 2</a>