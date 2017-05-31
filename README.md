# SlideLayout for Android

[![License](https://img.shields.io/badge/license-Apache%202-green.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[ ![Download](https://api.bintray.com/packages/dsiner/maven/slidelayout/images/download.svg) ](https://bintray.com/dsiner/maven/slidelayout/_latestVersion)

## Demo
![](https://github.com/Dsiner/SlideLayout/tree/master/screenshot/screenshot.gif)

## Setup
Maven:
```xml
<dependency>
  <groupId>com.dsiner.lib</groupId>
  <artifactId>slidelayout</artifactId>
  <version>1.0.0</version>
</dependency>
```
or Gradle:
```groovy
compile 'com.dsiner.lib:slidelayout:1.0.0'
```


## Usage
```xml
    <!--just contain two view-->
    <com.d.lib.slidelayout.SlideLayout
        android:layout_width="match_parent"
        android:layout_height="65dp">

        <!--content view-->
        <View
            android:layout_width="match_parent"
            android:layout_height="match_parent" />

        <!--slide view-->
        <View
            android:layout_width="wrap_content"
            android:layout_height="match_parent" />
    </com.d.lib.slidelayout.SlideLayout>
```

#### Operation
```java
        void open();
        void close();
        void setOpen(boolean open, boolean withAnim);
        boolean isOpen();
```

#### SetListener
```java
        slideLayout.setOnStateChangeListener(new SlideLayout.OnStateChangeListener() {
            @Override
            public void onChange(SlideLayout layout, boolean isOpen) {
            }

            @Override
            public boolean closeAll(SlideLayout layout) {
                return false;
            }
        });
```


More usage see [Demo](app/src/main/java/com/d/slidelayout/MainActivity.java)


## Licence

```txt
Copyright 2017 D

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
