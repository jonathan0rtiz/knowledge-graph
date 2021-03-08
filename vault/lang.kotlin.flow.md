---
id: 8329be9a-ca86-4c4a-a0b3-bff7fda2410f
title: Flow
desc: ''
updated: 1613354101119
created: 1613335969200
---

# Flow Control
```kotlin
if (booleanValIsTrue) {
    show()
} else {
    hide()
}
````

### When Statement
Kotlin when statement is the equivalent of a switch statment in other languages such as Java.

```java
// Java switch statement
int num = 3
switch (num) {
    case 1:
        System.out.println("One");
        break;
    case 2:
        System.out.println("Two");
        break;
    case 3:
        System.out.println("Three");
        break;
    default:
        System.out.println("Number not found.");
}
```
Output: `Three`

```kotlin
// Kotlin when statement
val num = 3
when (num) {
    1 -> println("One")
    2 -> println("Two")
    3 -> println("Three")
    else -> println("Number not found")
}
```
Output: `Three`