# OneDrawable

[![Build Status](https://travis-ci.org/maoruibin/OneDrawable.svg?branch=master)](https://travis-ci.org/maoruibin/OneDrawable)
[![](https://img.shields.io/hexpm/l/plug.svg)](https://github.com/maoruibin/OneDrawable/blob/master/LICENSE.txt)
[![](https://jitpack.io/v/maoruibin/OneDrawable.svg)](https://jitpack.io/#maoruibin/OneDrawable)

![OneDrawable](http://7xr9gx.com1.z0.glb.clouddn.com/slogin.gif)

Only use one drawable/color resource to set the background of the View. | [OneDrawable - 仅使用一张资源图片为 View 设置具有按下效果的背景](http://gudong.name/2017/04/05/OneDrawable.html)

## Sample
Please see the [sample app](https://github.com/maoruibin/OneDrawable/tree/master/app/src/main/java/name/gudong/demo) for a library usage example.

[sample apk](https://fir.im/leku)

shot 

![demo](http://7xr9gx.com1.z0.glb.clouddn.com/statebackgroundv2.gif)

## Gradle

```
dependencies {
    compile 'name.gudong:one-drawable:1.1.1'
}
```

## Usage
common usage

```java
Drawable drawable = OneDrawable.createBgDrawable(this,R.drawable.ic_action_name);
tvIcon1.setBackgroundDrawable(drawable);
```

## common api

 * createBgDrawable (use drawable resource create a background)
 * createBgColor (use color resource create a background)

### indicate pressed mode

pressed state with dark mode. In this mode, drawable will automatically cover a layer of dark when pressed.

drawable background

```java
Drawable icon1 = OneDrawable.createBgDrawableWithDarkMode(this,R.drawable.ic_action_name);
tvIcon1.setBackgroundDrawable(icon1);
```

color background 

```java
Drawable color2 = OneDrawable.createBgColor(this,R.color.colorAccent);
tvColor2.setBackgroundDrawable(color2);
```

pressed state with alpha mode. In this mode, drawable will automatically change alpha value to 0.7 when pressed.

```java
Drawable icon3 = OneDrawable.createBgDrawableWithAlphaMode(this,R.drawable.ic_action_add);
tvIcon3.setBackgroundDrawable(icon3);
```

### Custom Alpha value

Sometimes, maybe you need custom alpha value, you can use methods like follows.
 
```java
Drawable icon2 = OneDrawable.createBgDrawableWithDarkMode(this,R.drawable.ic_action_add,0.4f);
tvIcon2.setBackgroundDrawable(icon2);

Drawable icon4 = OneDrawable.createBgColorWithAlphaMode(this,R.drawable.ic_action_name,0.3f);
tvIcon4.setBackgroundDrawable(icon4);

Drawable icon4 = OneDrawable.createBgColorWithDarkMode(this,R.color.colorAccent,0.3f);
tvIcon4.setBackgroundDrawable(icon4);


Drawable icon4 = OneDrawable.createBgColorWithAlphaMode(this,R.color.colorAccent,0.3f);
tvIcon4.setBackgroundDrawable(icon4);

``` 

Note: `Because of only clickable view show it's pressed drawable, so you should set view clickable as true before you want to watch pressed effect.`

## Author
[http://gudong.name](http://gudong.name)

[https://github.com/maoruibin](https://github.com/maoruibin)

[http://weibo.com/maoruibin](http://weibo.com/maoruibin)

## License

    Copyright 2017 GuDong

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



