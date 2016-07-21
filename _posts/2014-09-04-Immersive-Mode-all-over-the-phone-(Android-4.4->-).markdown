---
title: Immersive Mode all over the phone (Android 4.4 > )
layout: post
date: 2014-09-04 20:08:00 UTC
updated: 2015-02-08 19:42:28 UTC
comments: false
categories: Android
---
What I tried was creating a transparent Activity that remains on top of all apps and using a service and a floating widget I send orders to the activity to enable or disable the immersive mode.<br /><br />There are some problems avoiding events like touch (see over whatsapp).<br /><br />If someone wants to continue.... theres the code:<br /><br /><a href="https://github.com/MakinGiants/android_full_immersive_mode">Github</a>