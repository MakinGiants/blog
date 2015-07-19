---
title: Code signing request failed because this file has been previously signed  Blackberry with Android app
layout: post
date: 2012-11-16 15:02:00 UTC
updated: 2015-02-08 19:42:30 UTC
comments: false
categories: Blackberry Android Port
---
If you get this error is because you are trying to sign an already signed version of your app.<div><br /></div><div>Go to android manifest and change versionCode +1 each time you want to sign your app.</div><div><br /></div><div><a href="http://supportforums.blackberry.com/t5/Testing-and-Deployment/Code-signing-request-failed-because-this-file-has-been/ta-p/798291">Source</a><br /><br /></div>