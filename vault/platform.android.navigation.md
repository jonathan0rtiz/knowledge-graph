---
id: cJhjKuWoRtEp8PmUH5iYO
title: Navigation
desc: ''
updated: 1633486093461
created: 1632180362940
---

The navigation component is a library that can manage complex navigation, transition animation, deep linking, and compile-time checked arguments passing between screens in your app.


```groovy
dependencies {
  ...
  implementation "androidx.navigation:navigation-fragment-ktx:$navigationVersion"
  implementation "androidx.navigation:navigation-ui-ktx:$navigationVersion"
  ...
}
```

#### Pop behavior for navigation actions
- `popUpTo` attribute of an action "pops ups" the back stack to a given destination before navigating.
- If the `popUpToInclusive` flag is `false` or not set, `popUpTo` removes destinations up to the specified destination, but leaves the specified destination in the back stack.


#### Summary
https://developer.android.com/codelabs/kotlin-android-training-add-navigation#11