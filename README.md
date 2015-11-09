# Wrap LayoutManager

![](art/android-wrap-layout-manager.png)

## Description

* Implementation of [LinearLayoutManager](https://developer.android.com/reference/android/support/v7/widget/LinearLayoutManager.html) which wraps its contents.
* Implementation of [GridLayoutManager](https://developer.android.com/reference/android/support/v7/widget/GridLayoutManager.html) which wraps its contents.

Usage example:

```java
final WrapLinearLayoutManager layoutManager = new WrapLinearLayoutManager(this, LinearLayoutManager.VERTICAL, false);
final RecyclerView recyclerView = (RecyclerView) findViewById(R.id.recyclerview);
recyclerView.setLayoutManager(layoutManager);
recyclerView.addItemDecoration(new DividerItemDecoration(this, null));
recyclerView.setAdapter(adapter);
```

Note that if the child views in your `RecyclerView` have the fixed size `LinearLayoutManager#setChildSize` should be used
to avoid unnecessary measuring.

## Installation

build.gradle via jcenter:

```gradle
repositories {
    // ...
    jcenter()
}

dependencies {
    // ...
    compile 'com.infstory:android-wrap-layout-manager:0.0.6'
}
```

build.gradle via jitpack:

```gradle
repositories {
    // ...
    maven { url "https://jitpack.io" }
}

dependencies {
    // ...
    compile 'com.github.yongjhih:android-wrap-layout-manager:-SNAPSHOT'
}
```

## License

Library is distributed under Apache 2.0 license, see LICENSE.txt

## Applications

The following applications use this library:
* [Sample app](https://oss.sonatype.org/content/repositories/releases/org/solovyev/android/views/linear-layout-manager-app/)
* [Say it right!](https://play.google.com/store/apps/details?id=org.solovyev.android.dictionary.forvo)
