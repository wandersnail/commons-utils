## 代码托管
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/cn.wandersnail/common-utils/badge.svg)](https://maven-badges.herokuapp.com/maven-central/cn.wandersnail/common-utils)
[![Download](https://api.bintray.com/packages/wandersnail/android/common-utils/images/download.svg) ](https://bintray.com/wandersnail/android/common-utils/_latestVersion)


## 使用

1. module的build.gradle中的添加依赖，自行修改为最新版本，需要哪个就依赖哪个，同步后通常就可以用了：
```
dependencies {
	...
	implementation 'cn.wandersnail:common-utils:latestVersion'
	implementation 'cn.wandersnail:common-base:latestVersion'
}
```

2. 如果从jcenter下载失败。在project的build.gradle里的repositories添加内容，最好两个都加上，添加完再次同步即可。
```
allprojects {
	repositories {
		...
		mavenCentral()
		maven { url 'https://dl.bintray.com/wandersnail/androidx/' }
	}
}
```