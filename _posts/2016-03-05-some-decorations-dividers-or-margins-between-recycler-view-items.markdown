---
title: Some decorations (dividers or margins) between recycler view items
layout: post
categories: Android, Kotlin
---

If you want to add margins between `RecyclerView` items you need to use a `RecyclerView.ItemDecoration`.

```java
recyclerView.setItemDecorator( /*your decorator instance*/ )
```

You can find some useful decorators here:

{% gist /caipivara/121b116add8fbc3af615 %}
