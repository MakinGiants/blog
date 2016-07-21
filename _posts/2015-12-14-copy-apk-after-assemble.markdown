---
title: Copy apks after assemble into some folder
layout: post
date: 2015-12-14
categories: Android, Gradle
---

If you want to copy the apks after assembling them you can create
a custom copy gradle task with something like:

{% gist danielgomezrico/bfb2fb5732d760e766f5 %}

This example use a gradle variable `TEST_BACKUP` to define where the backup will
be done.

Then you can call `./gradlew backupApks` or `./gradlew clean assemble backupApks`.
and see the copied apks there.
