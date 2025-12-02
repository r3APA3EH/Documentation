---
sidebar_position: 2
description: ""
---

# How to add the library to your mod's project
Gradle Properties:
```
pal_version = 1.1.1+mc.1.21.9
```
There is also a 1.21.1 version!: `pal_version = 1.1.1+mc.1.21.1`  
There is also a 1.21.7-8 version, but it's no longer supported, so I don't recommend using it.

Maven Repository:
```
        mavenCentral()
        maven {
            name = "RedlanceMinecraft"
            url = "https://repo.redlance.org/public"
        }
```

Architectury Common:
```
    modApi "com.zigythebird.playeranim:PlayerAnimationLibCommon:$rootProject.pal_version"
```

Architectury NeoForge:
```
    modImplementation "com.zigythebird.playeranim:PlayerAnimationLibNeo:$rootProject.pal_version"
```

Fabric:
```
    modImplementation "com.zigythebird.playeranim:PlayerAnimationLibFabric:$project.pal_version"
```

NeoForge:
```
    implementation "com.zigythebird.playeranim:PlayerAnimationLibNeo:$project.pal_version"
```