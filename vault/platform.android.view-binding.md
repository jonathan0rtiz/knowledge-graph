---
id: aRkMnsN8hKAKRxdb77ijn
title: View Binding
desc: ''
updated: 1633191226927
created: 1633190928945
---

View binding is a feature that allows you to more easily write code that interacts with views. Once view binding is enabled in a module, it generates a binding class for each XML layout file present in that module. An instance of a binding class contains direct references to all views that have an ID in the corresponding layout.

**In most cases, view binding replaces findViewById.**

#### Setup:
module-level `build.gradle`
```groovy
android {
    ...
    buildFeatures {
        viewBinding true
    }
}
```


