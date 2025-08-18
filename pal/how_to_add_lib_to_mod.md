---
sidebar_position: 2
---

# How to add the library to your mod's project
Gradle Properties:
```
pal_version = 1.0.7+mc1.21.7
```

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
    forgeRuntimeLibrary "org.javassist:javassist:3.30.2-GA"
```

Fabric:
```
    modImplementation "com.zigythebird.playeranim:PlayerAnimationLibFabric:$project.pal_version"
```

NeoForge:
```
    implementation "com.zigythebird.playeranim:PlayerAnimationLibNeo:$project.pal_version"
    additionalRuntimeClasspath "org.javassist:javassist:3.30.2-GA"
```