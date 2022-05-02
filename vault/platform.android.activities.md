---
id: 19c1309f-66c0-4adf-b942-8783e4fc8412
title: Activities
desc: ''
updated: 1651445807901
created: 1613334675829
---

An Activity is a single, focused thing that a user can do. Every app must have at least one Activity as its entry point. This of this entry-point Activity as the `main()` function in other programs.

The `AndroidManifest.xml` file includes details that the Android system needs in order to run your app, including what **activities** are part of your app. 

Each activity has an associated layout file. The activity and the layout are connected by a process known as *layout inflation*. When the activity starts, the views that are defined in the XML layout files are turned into (or "inflated" into) Kotlin view objects in memory. Once this happens, the activity can draw these objects to the screen and also dynamically modify them.

#### Gradle
Gradle is a build automation system that uses a domain-specific language to describe the app's project structure, configuration, and dependencies. When you compile and run you r app, you see information about the Gradle build running. You also see information about the Android Package Kit (APK) being installed.

