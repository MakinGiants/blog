---
title: Add Mixins to View in Sencha Architec SA 2
layout: post
date: 2013-08-09 12:51:00 UTC
updated: 2015-02-08 19:42:29 UTC
comments: false
categories: Extjs Sencha Architect
---
By Default you will not be able to see the mixins property in the inspector of the <i>View</i>, and if you try to add it as custom it will show "<i>Attempted to add a property that already exist</i>".<br /><br /><span style="font-size: large;">But you can do one thing:</span><br /><br /><ol><li>Right click on the view and "<i>Promote to class</i>" and it will create another js inside the projects.</li><li>Go again to the <i>View</i> and see the new property in the &nbsp;inspector "<i>mixins</i>"</li><li>Add the properties you want to mix.</li></ol>Mixins Value Example:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> {  <br />   dragSelector: 'Ext.ux.DataView.DragSelector',  <br />   draggable  : 'Ext.ux.DataView.Draggable'  <br /> }  <br /></code></pre><br />And thats all...