---
id: 46c50cd1-8dcf-4bf3-9eea-20f7a129456f
title: Arrays
desc: ''
updated: 1640806249213
created: 1613342382107
---

Arrays in Kotlin are represented by the `Array` class.
```kotlin
val arr = arrayOf<Int>(1, 2, 3) // [1, 2, 3]
```

**Primitive Array's - Kotlin**
- Kotlin also has classes that represent arrays of primitive types without boxing overhead: `ByteArray`, `ShortArray`, `IntArray`, and so on.

- These classes have no inheritance relation to the `Array` class, but they have the same set of methods and properties. Each of them also has a corresponding factory function.

```kotlin
val x: IntArray = intArrayOf(1, 2, 3)
```
#### Array Declaration + Initialization
```kotlin
val arrayName = Array(5) { 0 } // [0, 0, 0, 0, 0]
```

#### Accessing elements in an Array
```kotlin
// Just traversing
for (i in arrayName) {
    println(i)
}
// Using range
for (i in 0..arrayName.size - 1) {
    println(arrayName[i])
}
// range with step
for (i in 0..arrayName.size - 1 step 2) {
    println(arrayName[i])
}
```