---
title: Install android build tools on custom server to build android projects
layout: post
categories: Android, CI
author: caipivara
---

This may help if you want to make your own local device test farm with gitlab or something.

Some time ago we were able to download a the hole package of android build things/tools from android page.
Now we have just `android-sdk/tools` and there `../tools/bin/sdkmanager` tool to download what we need.

1. Download and setup _android tools_:

{% gist caipivara/1109a5feeedcb4f8d6c74f43a4e29dbc readme.md %}

2. Install what you need with one of those:

_Note: you need to accept linceses manually _

{% gist caipivara/1109a5feeedcb4f8d6c74f43a4e29dbc install-deps-with-sdkmanager.sh %}

{% gist caipivara/1109a5feeedcb4f8d6c74f43a4e29dbc install-deps-with-android.sh %}