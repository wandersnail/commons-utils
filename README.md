## 代码托管
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/cn.wandersnail/common-utils/badge.svg)](https://maven-badges.herokuapp.com/maven-central/cn.wandersnail/common-utils)
[![Download](https://api.bintray.com/packages/wandersnail/androidx/common-utils/images/download.svg) ](https://bintray.com/wandersnail/androidx/common-utils/_latestVersion)


## 使用
1. 因为使用了jdk8的一些特性，需要在module的build.gradle里添加如下配置：
```
//纯java的项目
android {
	compileOptions {
		sourceCompatibility JavaVersion.VERSION_1_8
		targetCompatibility JavaVersion.VERSION_1_8
	}
}

//有kotlin的项目还需要在project的build.gradle里添加
allprojects {
    tasks.withType(org.jetbrains.kotlin.gradle.tasks.KotlinCompile).all {
        sourceCompatibility = JavaVersion.VERSION_1_8
        targetCompatibility = JavaVersion.VERSION_1_8

        kotlinOptions {
            jvmTarget = '1.8'
            apiVersion = '1.3'
            languageVersion = '1.3'
        }
    }
}

```
2. module的build.gradle中的添加依赖，自行修改为最新版本，需要哪个就依赖哪个，同步后通常就可以用了：
```
dependencies {
	...
	implementation 'cn.wandersnail:common-utils:latestVersion'
	implementation 'cn.wandersnail:common-base:latestVersion'
}
```

3. 如果从jcenter下载失败。在project的build.gradle里的repositories添加内容，最好两个都加上，添加完再次同步即可。
```
allprojects {
	repositories {
		...
		mavenCentral()
		maven { url 'https://dl.bintray.com/wandersnail/androidx/' }
	}
}
```
