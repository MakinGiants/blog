---
title: Change apk name
layout: post
date: 2015-12-14
categories: Android, Gradle
---

If you want to add the version or build number to your apk to save them and have
some kind of backup for apks you can use `archivesBaseName` property that
define a prefix for the apk names in your `defaultConfig`.

{% gist caipivara/902320c9e8e14be5f4d4 %}

Results: `app-1.0.0-12-<buildType>-<flavor>.apk`
