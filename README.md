# DigitSpeedView
[![](https://jitpack.io/v/Cogosense/DigitSpeedView.svg)](https://jitpack.io/#Cogosense/DigitSpeedView)

Awesome digital speedometer for android, [see project on GitHub](https://github.com/Cogosense/DigitSpeedView).
Original project - [see ioriginal project on GitHub](https://github.com/capur16/DigitSpeedView).

<img src="images/DigitSpeedView1.png" width="33%" />
<img src="images/DigitSpeedView2.png" width="33%" />
<img src="images/DigitSpeedView3.png" width="33%" />

Compatibility
-------------

This library is compatible from API 14 (Android 4.0).

Download
-------------

**add this line to** `build.gradle`

```gradle

allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}

```

**add this line to** `app/build.gradle`

```gradle

dependencies {
    compile 'com.github.Cogosense:digitspeedviewlib:1.0.5'
}

```

Simple Usage
-------------
add DigitSpeedView to your `Layout.xml`.<br>
```xml

<com.github.capur16.digitspeedviewlib.DigitSpeedView
            android:id="@+id/digit_speed_view"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            app:speed="16" />

```

Advanced Usage
-------------

```xml

<com.github.capur16.digitspeedviewlib.DigitSpeedView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                app:backgroundColor="@color/my_background_color"
                app:disableBackgroundImage="false"
                app:showUnit="true"
                app:backgroundDrawable="@drawable/my_background_image"
                app:speed="30"
                app:speedTextColor="@android:color/holo_blue_light"
                app:speedTextSize="20dp"
                app:unit="mph"
                app:unitTextColor="@android:color/holo_blue_light"
                app:unitTextSize="5dp" />

```

Update Speed From Java
-------------

```
DigitSpeedView digitSpeedView = (DigitSpeedView)findViewById(R.id.digit_speed_view);
digitSpeedView.updateSpeed(120);
```

OnSpeedChangeListener
-------------

```
DigitSpeedView digitSpeedView = (DigitSpeedView)findViewById(R.id.digit_speed_view);
digitSpeedView.setOnSpeedChangeListener(new OnSpeedChangeListener() {
    @Override
    public void onSpeedChange(DigitSpeedView digitSpeedView, boolean isSpeedUp) {
        //Current speed: digitSpeedView.getSpeed();
    }
});
```

License
-------

    Copyright 2017 Riccardo Capuani

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
       http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
