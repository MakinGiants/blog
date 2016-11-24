---
title: Fix first time with shared element transition theres no animation using picasso or oher image loading lib (dont work)
layout: post
---

You need to call `supportPostponeEnterTransition()` on create to wait until `Picasso` have the image loaded and then start the posponed animation with 
`supportStartPostponedEnterTransition`.

Using picasso you can do you it using a `Callback` like:

{% gist /caipivara/3687f79328dcf7bfc98c %}

Thanks to [androiddesignpatterns](http://www.androiddesignpatterns.com/2015/03/activity-postponed-shared-element-transitions-part3b.html)