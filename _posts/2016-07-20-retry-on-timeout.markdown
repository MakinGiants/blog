---
title: Retry multiple times on timeout with RxJava for Kotlin (or java)
layout: post
categories: Android, io

---

The idea is to use `retryWhen` _RxJava_ function to create a new timber _observable_ if it's a timeout on error

A _copy/paste_ solution can be found in:

{% gist /danielgomezrico/5f585df16b5a4722e1747a324b70e2b8 RetryWithDelayIfTimeout.kt %}

It's just a custom `Func1` that receives an `Observable` to watch for errors with `flatMap` that should be used with `retryWhen` operator. For every retry it will wait _+1 seconds_

# Sample

To retry 3 times with 2 initial delay seconds, you must use something like: 

```
myObservable.retryWhen(RetryWithDelayIfTimeout(3, 2))
            .subscribe(...)
```

# Extra

If you want to make it cleaner, add `io()` and `MainThread()` management (every io call have it) you can use something like:

{% gist /danielgomezrico/5f585df16b5a4722e1747a324b70e2b8 ObservableExtensions.kt %}

and then apply it everywhere:

{% gist /danielgomezrico/5f585df16b5a4722e1747a324b70e2b8 Usage.kt %}

Written in Kotlin but you can make `java` versions easy.

# Thanks to
- [Danlew rxjavas-repeatwhen-and-retrywhen-explained](http://blog.danlew.net/2016/01/25/rxjavas-repeatwhen-and-retrywhen-explained/)

