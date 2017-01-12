---
title: How to display FAB with right margins on all devices
layout: post
categories: Android, MaterialDesign
---

If you use marinBottom="16dp" for _FABs_ you will have problems between versions since `Fab`

You can use `app:useCompatPadding=“true”` on your `FAB` so it knows when to use `16dp` or `0dp` based on the Android OS for you.

{% gist caipivara/a599de05772577f3c605790001a044ed %}

_ps: thanks to `AppCompat` guys that are making our dev life ultra awesome_.