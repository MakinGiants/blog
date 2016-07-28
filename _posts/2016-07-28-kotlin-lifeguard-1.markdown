---
title: KotlinLifeguard "#1
layout: post
categories: Android, Kotlin
---

Using [@JvmOverloads][0] tag helps to avoid multiple constructors with Kotlin

## The headache

It's really possible that you had some code like:

{% gist danielgomezrico/e51337945d9277e6c5ad95e1abe33daf with-problem.kt %}

As you can see there are all the constructors needed for a _custom_ `FrameLayout` but all with same "body".

![]( {{ site.path-emoji-hmm }} )
 
# The remedy

Refactored with `@JvmOverloads`:

{% gist danielgomezrico/e51337945d9277e6c5ad95e1abe33daf fixed.kt %}

## Thanks to

- [Kotlin discuss](https://discuss.kotlinlang.org/t/simple-constructors-for-inheritance/1874/2)


[0]: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.jvm/-jvm-overloads/