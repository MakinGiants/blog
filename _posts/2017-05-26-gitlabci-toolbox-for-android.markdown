---
title: Gitlab-ci Toolbox for Android
layout: post
categories: Android CI
author: caipivara
---

You can setup your own CI server with real devices on gitlab with these scripts and setups.
I found this issues that are common between any CI server:

- Copy env/secret variables to local project before each run.
- Run commands on every device connected.
- Run tests with test coverage and see it inside gitlab-ci.
- Install app dependencies before each run if needed.
- You need to setup ([How to][0]) your gitlab runner executor to `shell` to make it run processes "natively" instead of start a new Docker instance for every test.

## 1. Gitlab will run everything you put in `.gitlab-ci.yml`, check this sample:

{% gist caipivara/33d35da315cedf795e01f168e8525e1d .gitlab-ci.yml %}

- I use spoon to run UI tests, update the gradle task in case you use another thing.
- All scripts in `scripts/` will be explained in **3.** .

## 2. Android project setup:

- Setup code coverage, tests and spoon:
{% gist caipivara/33d35da315cedf795e01f168e8525e1d build.gradle %}

- Setup jacoco tasks to generate code coverage files:
{% gist caipivara/33d35da315cedf795e01f168e8525e1d jacoco.gradle %}

- Setup tests to print each test result (to see in the job results which ones failed)
{% gist caipivara/33d35da315cedf795e01f168e8525e1d test-setup.gradle %}

## 3. Usefull scripts:

- Install your project dependencies on the machine by terminal:
{% gist caipivara/33d35da315cedf795e01f168e8525e1d install-android-dependencies.sh %}

- Run the same command on every connected device (avoid INSTALL_FAILED_UPDATE_INCOMPATIBLE)
{% gist caipivara/33d35da315cedf795e01f168e8525e1d adb-all.sh %}

- Copy every env/secret variable into `gradle.propertes` file inside the project (gmaps key or something like that)
{% gist caipivara/33d35da315cedf795e01f168e8525e1d cp-env-to-properties.sh %}


## Gitlab-ci Advantages:
- "Free" testing farm (your own devices, maybe uncle/grandmother/mom old devices).
- "Free" Parallel Job Executions based on your machine (you can setup your gitlab-ci runner to allow this).
- "Secure" handling of signing keys (it depends to you).
- "Secure" handling of services config keys (like google console config jsons).
- Fastest test/build/everything jobs since gradle daemon can run in your machine (on CircleCi/Travis/Etc you need to disable it since they start a new virtual machine for every test).

# Links

- [How to setup your gitlab runner guide][0]
- [How to setup gitlab for android projects][1]

[0] : http://docs.gitlab.com/runner/register/
[1] : https://about.gitlab.com/2016/11/30/setting-up-gitlab-ci-for-android-projects/

Now enjoy a happy android dev :)