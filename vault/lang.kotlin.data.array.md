---
id: 46c50cd1-8dcf-4bf3-9eea-20f7a129456f
title: Arrays
desc: ''
updated: 1623200912801
created: 1613342382107
---

Arrays in Kotlin are represented by the `Array` class.
```kotlin
val arr = arrayOf<Int>(1, 2, 3) // [1, 2, 3]
```

**Primitive Array's**
Kotlin also has classes that represent arrays of primitive types without boxing overhead: `ByteArray`, `ShortArray`, `IntArray`, and so on.

These classes have no inheritance relation to the `Array` class, but they have the same set of methods and properties. Each of them also has a corresponding factory function.
```kotlin
val x: IntArray = intArrayOf(1, 2, 3)
```