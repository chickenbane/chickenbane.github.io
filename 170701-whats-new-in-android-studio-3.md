
## Build Speed

A major theme in 3.0 is improving build speed.  Accordingly, the Android Gradle Plugin introduced breaking changes to facilitate the speed increases.

## Profiler

## Layout Editor

## Architecture Components

## D8

Because Android is open source and code is awesome I took a look at these programs to see if I could answer some of these questions.

Immediate observations:
* A big change in Gradle 4.1 is the Worker API.  Builds are getting more complex in multiple dimensions.
https://youtu.be/jp_Dv4VjVWE?t=17m15s
Worker API
* In project parallelism
* remote workers: 
  * own vm
  * long lived, warm and jitted
* these also do their own gc, so doing a gc doesn't kill your build speed
  * started killed based on machine load
* one configuration for ci servers with a ton of ram

* all about proguard
  * d8 is actually part of the r8 project, which should appropriately indicate what the bigger problem is
* r8 really needs to be part of the android plugin to get big speed improvements.  r8 needs a lot of ram so having it separate either kills your build or (more often) wastes your memory because you usuually don't run proguard.
* timing.  right after gradle 4.1 is released.  AS3.0 must depend o Gradle 4.1 anyway.  this will probably be rolled out very soon.  aosp is using it!  no dsl impact or even knobs.
* more work to do. easily you can see how this can make more tasks cacheable. seems to be some

If you have been avoiding using the canary builds because you only use stable: With the AS change from alpha and beta, if you maintain android builds I think now is a good time to start migrating.  The features and DSL aren't changing drastically -
 converting my (purposely simple builds) to 3.0 wasn't difficult and when you understand the improvements it will make your daily build/run cycle it's really worth it.  Looks like most of the major Studio features - amazing (!) profiler, device explorer, aren't changing so try it out! Luckily tools team made this easy to parallel install, disk space is cheap, and learn the stuff you're using.
 
 https://android.googlesource.com/platform/dalvik/+/a9ac3a9d1f8de71bcdc39d1f4827c04a952a0c29/dx/src/com/android/dx/command/dexer/Main.java