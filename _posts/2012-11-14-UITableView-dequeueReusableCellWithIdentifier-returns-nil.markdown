---
title: UITableView dequeueReusableCellWithIdentifier returns nil
layout: post
date: 2012-11-14 23:13:00 UTC
updated: 2015-02-08 19:42:31 UTC
comments: false
categories: IOS
---
<i><span style="color: red;">ONLY WORKS WITH IOS &gt;= 5.0 so see&nbsp;<a href="http://www.makingiants.com/2012/11/check-ios-version-number-or-running.html">Check IOS Version Tutorial</a>&nbsp;to check this before.</span></i><br /><br />You need to register the nib file to be ready to be reused with:<br /><br /><pre style="background-image: URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif); background: #f0f0f0; border: 1px dashed #CCCCCC; color: black; font-family: arial; font-size: 12px; height: auto; line-height: 20px; overflow: auto; padding: 0px; text-align: left; width: 99%;"><code style="color: black; word-wrap: normal;"> static NSString* CellIdentifier = @"CellIdentifierName";  <br /> [tableview registerNib:[UINib nibWithNibName:@"nibfilename" bundle:nil] forCellReuseIdentifier:CellIdentifier];  </code></pre><br /><a href="http://www.ioslearner.com/features-uitableview-ios-5/#more-119">Source</a><br /><div><br /><br /><h3><span style="font-size: large;">Usefull links</span></h3><i><span style="color: red;"><a href="http://www.makingiants.com/2012/11/check-ios-version-number-or-running.html">Check IOS Version Tutorial</a>&nbsp;</span></i></div>