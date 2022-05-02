---
id: BzU4ZDaosCppZOfPNSE26
title: Coroutines
desc: ''
updated: 1637549755808
created: 1637538187249
---

Concurrency allows multiple units of code to execute out of order or seemingly in parallel permitting more efficient use of resources.

![](/assets/images/2021-11-21-19-04-32.png)

#### Race Condition
When multiple threads try to access the same value in memory in at the same time. Race conditions can result in hard to reproduce, random looking bugs, which may cause your app to crash, often unpredictably.

#### Coroutines
- Job:
    - A cancelable unit of work with a lifecycle inside a `CoroutineScope`, such as one created with the `launch()` function.


- CoroutineScope:
    - A context that enforces cancellation and other rules to its children and their children recursively. Functions used to create new coroutines such as **launch** and **async** extend **CoroutineScope**.


- Dispatcher: 
    - Manages which backing thread the coroutine will use for its execution. The **Main** dispatcher will always run coroutines on the main thread.

- launch():
    - this function creates a coroutine from the enclosed code wrapped in a cancellable Job object.

    - `launch()` is used when a return value is not needed outside of the confines of the coroutine.

    - `suspend`: The block of code passed to launch is marked with the `suspend` keyword. Suspend signals that a block of code can be paused or resumed.
    > - Whenever a function calls a another `suspend` function, then it should also be a `suspend` function.
    > - If a function does not call a `suspend` function, then it does not need to be a `suspend` function itself.
    
    ```kotlin
    fun CoroutineScope.launch {
        context: CoroutineContext = EmptyCoroutineContext,
        start: CoroutineStart = CoroutineStart.DEFAULT,
        block: suspend CoroutineScope.() -> Unit
    }
    ```

- runBlocking():
    - starts a new coroutine and blocks the current thread until completion.

- async():
    - Returns a value of type `Deferred`. A `Deferred` is a cancellable `Job` that can hold a reference to a future value.


**Resources**

https://developer.android.com/codelabs/basic-android-kotlin-training-introduction-coroutines?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-kotlin-unit-4-pathway-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-training-introduction-coroutines#6

**Learn more:**

Thread: https://developer.android.com/reference/java/lang/Thread