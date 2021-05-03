Repro to show kapt compile error with configuration cache enabled.

```
Configuration cache is an incubating feature.
Reusing configuration cache.

> Task :app:kaptGenerateStubsDebugKotlin FAILED
e: Source file or directory not found: /Users/michael_dang/AndroidStudioProjects/ConfigCacheRepro/app/src/main/java/com/example/configcacherepro/NewClass.kt

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:kaptGenerateStubsDebugKotlin'.
> Compilation error. See log for more details
```

Steps to repro:
1. Build with `./gradlew app:assembleDebug`. Observe build success and Config Cache entry stored
2. Delete `NewClass.kt`
3. Build again and observe error
