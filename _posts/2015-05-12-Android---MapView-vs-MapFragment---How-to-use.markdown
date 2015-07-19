---
title: Android - MapView vs MapFragment - How to use
layout: post
date: 2015-05-12 15:17:00 UTC
updated: 2015-05-12 15:17:25 UTC
comments: false
categories: Android
---

When you should use `MapFragment` or `MapView`? 

## [MapFragment](http://developer.android.com/reference/com/google/android/gms/maps/MapFragment.html)

* Use it if you want to add a map into Activity class (not fragment because it will create a nested fragment and it´s a mess).
* Use SupportMapFragment if you want to support just android versions lower than v12.

## [MapView](https://developers.google.com/android/reference/com/google/android/gms/maps/MapView)

* Use it if you are going to add a map into a fragment. (you need to update each lifecicle to MapView).